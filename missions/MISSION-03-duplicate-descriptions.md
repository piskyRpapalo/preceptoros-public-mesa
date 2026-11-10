# MISSION-03 · Detect duplicate public descriptions across repositories

**Mission ID:** MISSION-03  
**Status:** Open  
**Difficulty:** Low  
**Estimated time:** 30 minutes  
**Public information only:** Yes  

---

## Purpose

The PreceptorOS ecosystem maintains consistent terminology across repositories.
Duplicate or contradictory descriptions cause confusion for contributors and AI agents.
This mission compares the README introduction paragraphs of three public repositories.
The deliverable identifies exact duplicates, near-duplicates, and contradictions.

---

## Inputs

| Source | Type | URL |
|---|---|---|
| `preceptoros-web` | Public GitHub repository | https://github.com/piskyRpapalo/preceptoros-web |
| `preceptoros-app` | Public GitHub repository | https://github.com/piskyRpapalo/preceptoros-app |
| `study` | Public GitHub repository | https://github.com/piskyRpapalo/study |

---

## Scope

- Inspect only the `README.md` file at the root of each repository.
- Extract only the first prose paragraph below the first `# ` heading.
- Do not inspect any other file.
- Do not modify any file.

---

## Definitions

| Term | Definition |
|---|---|
| **Exact duplicate** | Two descriptions that are character-for-character identical. |
| **Near-duplicate** | Two descriptions that share more than 60% of their words (computed as word overlap divided by the larger word count). |
| **Contradiction** | Two descriptions that make opposite factual claims about the same named entity. Example: one says "local-first" and another says "cloud-based". |
| **Unique** | A description that shares fewer than 60% words with any other, and contains no contradiction. |

---

## Steps

Execute every step in order.

1. Clone each repository:

   ```
   git clone https://github.com/piskyRpapalo/preceptoros-web.git
   git clone https://github.com/piskyRpapalo/preceptoros-app.git
   git clone https://github.com/piskyRpapalo/study.git
   ```

2. Extract the first prose paragraph from each README:

   ```
   python3 -c "
   import sys, re
   text = open(sys.argv[1]).read()
   # skip the H1 heading, find first non-empty paragraph
   lines = text.splitlines()
   in_body = False
   para = []
   for line in lines:
       if line.startswith('# '):
           in_body = True
           continue
       if in_body:
           if line.strip() == '':
               if para:
                   break
           else:
               para.append(line.strip())
   print(' '.join(para))
   " <repo>/README.md
   ```

   Run once per repository. Record each extracted paragraph.

3. Compute the word overlap between every pair of paragraphs:

   ```
   python3 -c "
   a = set('''<paragraph A>'''.lower().split())
   b = set('''<paragraph B>'''.lower().split())
   overlap = len(a & b) / max(len(a), len(b)) if max(len(a), len(b)) > 0 else 0
   print(f'{overlap:.2%}')
   "
   ```

   Run for every pair: (web, app), (web, study), (app, study).

4. Classify each pair using the definitions above.

5. Scan each paragraph for contradictory key terms:

   Check whether the same repository characteristic appears with opposite values in two descriptions.
   Focus on these terms: `local-first`, `cloud`, `public`, `private`, `zero external requests`.

6. Record your receipt for each step:

   ```
   COMMAND: <exact command>
   OUTPUT:  <result>
   MACHINE: <machine type or NO_DATA — reason: not available>
   DATE:    <ISO 8601 date>
   PATH:    <file inspected>
   ```

---

## Deliverable

Place one file at: `missions/MISSION-03/deliverable.md`

The file must contain:

**Section 1 — Receipt.** One receipt block per step per repository.

**Section 2 — Extracted paragraphs.** Three labeled blocks:

```
### preceptoros-web
<extracted paragraph>

### preceptoros-app
<extracted paragraph>

### study
<extracted paragraph>
```

**Section 3 — Comparison table.** A Markdown table with these columns:

| Column | Description |
|---|---|
| `Pair` | The two repositories compared (e.g., `web / app`) |
| `Word_overlap` | Percentage, rounded to 2 decimal places |
| `Classification` | `EXACT_DUPLICATE`, `NEAR_DUPLICATE`, `UNIQUE`, or `NO_DATA — reason: <cause>` |
| `Contradiction_found` | `YES`, `NO`, or `NO_DATA — reason: <cause>` |
| `Contradiction_detail` | The contradictory terms, or `NONE` |

**Section 4 — Summary.**

```
TOTAL_PAIRS_CHECKED:    3
EXACT_DUPLICATES:       <integer>
NEAR_DUPLICATES:        <integer>
CONTRADICTIONS_FOUND:   <integer>
NO_DATA_COUNT:          <integer>
DATE:                   <ISO 8601 date>
```

---

## Acceptance criteria

The Sovereign verifies by running steps 2 and 3 on the same README files.
The extracted paragraphs must match.
The word overlap percentages must be within ±1% of the deliverable values (rounding differences are acceptable).
The `NO_DATA_COUNT` must equal the number of cells containing `NO_DATA`.

---

## Risks and prohibited operations

- Do not push, commit, or delete any file in any source repository.
- Do not send README content to any external similarity-scoring service.
- Do not rewrite or improve the README content. Describe only; do not change.
- Do not inspect any file other than `README.md` at the root of each repository.

---

## Required evidence

Each extracted paragraph must include the exact path and the commit SHA at the time of extraction:

```
COMMAND: git rev-parse HEAD
OUTPUT:  <SHA>
DATE:    <ISO 8601 date>
PATH:    <repo>/README.md
```

A deliverable without commit SHAs is incomplete.
The Sovereign will reject a deliverable that contains paragraphs not found in the source files.
