# MISSION-01 · Audit obsolete public links in `preceptoros-web`

**Mission ID:** MISSION-01  
**Status:** Open  
**Difficulty:** Low  
**Estimated time:** 30 minutes  
**Public information only:** Yes  

---

## Purpose

Markdown files in `preceptoros-web` contain hyperlinks.
Some links may point to renamed or deleted resources.
This mission identifies every broken or obsolete link in the repository's Markdown files.
The deliverable is a table that the Sovereign can use to plan corrections.

---

## Inputs

| Source | Type | URL |
|---|---|---|
| `preceptoros-web` | Public GitHub repository | https://github.com/piskyRpapalo/preceptoros-web |

---

## Scope

- Inspect all `*.md` files at the repository root.
- Do not inspect subdirectories.
- Do not inspect non-Markdown files.
- Do not modify any file.

---

## Steps

Execute every step in order.

1. Clone the public repository:

   ```
   git clone https://github.com/piskyRpapalo/preceptoros-web.git
   cd preceptoros-web
   ```

2. List all Markdown files at the root level:

   ```
   find . -maxdepth 1 -name "*.md" | sort
   ```

   Record the output.

3. Extract all hyperlinks from each file:

   ```
   grep -oP 'https?://[^\s\)\]"]+' *.md | sort -u
   ```

   Record every unique URL found.

4. Check the HTTP status code of each URL:

   ```
   curl -o /dev/null -s -w "%{http_code} %{url_effective}\n" --max-time 10 <URL>
   ```

   Run this command once per URL. Record the status code and URL.

5. Classify each URL using this table:

   | Code range | Label |
   |---|---|
   | 200–299 | `OK` |
   | 301, 302, 308 | `REDIRECT` |
   | 404 | `NOT_FOUND` |
   | 403 | `FORBIDDEN` |
   | Timeout / no response | `UNREACHABLE` |
   | Other | `OTHER_<code>` |

6. Record your receipt for each step:

   ```
   COMMAND: <exact command>
   OUTPUT:  <first 10 relevant lines>
   MACHINE: <machine type or NO_DATA — reason: not available>
   DATE:    <ISO 8601 date>
   PATH:    <file or URL inspected>
   ```

---

## Deliverable

Place one file at: `missions/MISSION-01/deliverable.md`

The file must contain:

**Section 1 — Receipt.** One receipt block per step (see format above).

**Section 2 — Link table.** A Markdown table with these columns:

| Column | Description |
|---|---|
| `Source_file` | The Markdown file that contains the link |
| `URL` | The full URL |
| `Status_code` | The HTTP status code, or `TIMEOUT`, or `NO_DATA` |
| `Label` | One of: `OK`, `REDIRECT`, `NOT_FOUND`, `FORBIDDEN`, `UNREACHABLE`, `OTHER_<code>` |

**Section 3 — Summary.**

```
TOTAL_LINKS_CHECKED: <integer>
BROKEN_OR_OBSOLETE:  <integer — count of rows where Label is not OK>
NO_DATA_COUNT:       <integer — count of rows where Status_code is NO_DATA>
DATE:                <ISO 8601 date>
```

Declare `NO_DATA — reason: <cause>` for every URL you cannot check.

---

## Acceptance criteria

The Sovereign verifies the deliverable by running step 4 independently on a sample of five URLs.
The labels must match within the same classification table.
The `NO_DATA_COUNT` must equal the number of rows where `Status_code` is `NO_DATA`.

---

## Risks and prohibited operations

- Do not push, commit, or delete any file in `preceptoros-web`.
- Do not follow redirect chains more than once.
- Do not submit URLs to any external scanning service.
- Do not publish authentication tokens, session cookies, or response bodies.
- If a URL requires authentication, classify it as `NO_DATA — reason: authentication required`.

---

## Required evidence

Every row in the deliverable must be traceable to a specific file and a specific `curl` command.
A row without a receipt is incomplete.
The Sovereign will reject a deliverable that contains invented status codes.
