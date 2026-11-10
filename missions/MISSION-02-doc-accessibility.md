# MISSION-02 · Review documentation accessibility in `study`

**Mission ID:** MISSION-02  
**Status:** Open  
**Difficulty:** Low  
**Estimated time:** 45 minutes  
**Public information only:** Yes  

---

## Purpose

The `study` repository is public doctrine.
Contributors and AI agents rely on it to understand the PreceptorOS ecosystem.
This mission checks whether the root-level Markdown files meet basic readability criteria.
The deliverable is a scored table that shows which files are easy to read and which need improvement.

---

## Inputs

| Source | Type | URL |
|---|---|---|
| `study` | Public GitHub repository | https://github.com/piskyRpapalo/study |

---

## Scope

- Inspect all `*.md` files at the repository root.
- Do not inspect subdirectories.
- Do not inspect non-Markdown files.
- Do not modify any file.

---

## Checks

Apply these four checks to every file:

| Check ID | Name | Pass condition |
|---|---|---|
| C1 | **H1 heading present** | The file contains exactly one `# ` heading at the top level. |
| C2 | **Short sentences** | No paragraph contains a sentence longer than 40 words. Count words by splitting on spaces. |
| C3 | **Active voice indicator** | The file does not use the phrases `is done by`, `was done by`, `are done by`, or `were done by`. |
| C4 | **NO\_DATA declared** | If the file contains `NO_DATA`, it always appears with a colon and a reason on the same line (e.g., `NO_DATA — reason:` or `NO_DATA:`). |

A file **passes** a check if the pass condition is true.
A file **fails** a check if the pass condition is false.
A file receives `NO_DATA — reason: <cause>` for a check you cannot run.

---

## Steps

Execute every step in order.

1. Clone the public repository:

   ```
   git clone https://github.com/piskyRpapalo/study.git
   cd study
   ```

2. List all Markdown files at the root level:

   ```
   find . -maxdepth 1 -name "*.md" | sort
   ```

   Record the count and the full list.

3. For each file, run check C1:

   ```
   grep -c "^# " <filename>
   ```

   A count of 1 is a pass. Any other count is a fail.

4. For each file, run check C2 (longest sentence word count):

   ```
   python3 -c "
   import re, sys
   text = open(sys.argv[1]).read()
   sentences = re.split(r'[.!?]', text)
   lengths = [len(s.split()) for s in sentences]
   print(max(lengths) if lengths else 0)
   " <filename>
   ```

   A result of 40 or fewer is a pass. A result above 40 is a fail.

5. For each file, run check C3:

   ```
   grep -iE "is done by|was done by|are done by|were done by" <filename>
   ```

   No output is a pass. Any output is a fail.

6. For each file, run check C4 (only if the file contains `NO_DATA`):

   ```
   grep "NO_DATA" <filename>
   ```

   Review each matching line. A line that contains `NO_DATA` without `:` or `—` is a fail.
   If the file contains no `NO_DATA`, mark C4 as `N/A`.

7. Record your receipt for each file and each check:

   ```
   COMMAND: <exact command>
   OUTPUT:  <result>
   MACHINE: <machine type or NO_DATA — reason: not available>
   DATE:    <ISO 8601 date>
   PATH:    <filename>
   ```

---

## Deliverable

Place one file at: `missions/MISSION-02/deliverable.md`

The file must contain:

**Section 1 — Receipt.** One receipt block per file per check.

**Section 2 — Accessibility table.** A Markdown table with these columns:

| Column | Description |
|---|---|
| `File` | Filename (basename only) |
| `C1_H1` | `PASS`, `FAIL`, or `NO_DATA — reason: <cause>` |
| `C2_Sentences` | `PASS`, `FAIL`, or `NO_DATA — reason: <cause>`. Include max word count. |
| `C3_Active` | `PASS`, `FAIL`, or `NO_DATA — reason: <cause>` |
| `C4_NO_DATA` | `PASS`, `FAIL`, `N/A`, or `NO_DATA — reason: <cause>` |
| `Overall` | `PASS` if all applicable checks pass. `FAIL` otherwise. |

**Section 3 — Summary.**

```
TOTAL_FILES_CHECKED:  <integer>
TOTAL_PASS:           <integer — files where Overall is PASS>
TOTAL_FAIL:           <integer — files where Overall is FAIL>
NO_DATA_COUNT:        <integer — cells where value starts with NO_DATA>
DATE:                 <ISO 8601 date>
```

---

## Acceptance criteria

The Sovereign verifies by running steps 3 through 6 on three files chosen at random.
The pass/fail results must match the deliverable.
The `NO_DATA_COUNT` must equal the number of cells containing `NO_DATA`.

---

## Risks and prohibited operations

- Do not push, commit, or delete any file in `study`.
- Do not use readability tools that send file content to external services.
- Do not rewrite or summarize file content in the deliverable.
- Do not apply checks to files outside the repository root.

---

## Required evidence

Every row in the table must have a receipt.
A receipt must show the exact command and its output.
A row without a receipt is incomplete.
The Sovereign will reject a deliverable that contains invented pass/fail values.
