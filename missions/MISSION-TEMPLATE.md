# MISSION-XX · [Short imperative title]

> [!NOTE]
> This is the reusable template for Public Mesa missions.
> Replace every `[placeholder]` before publishing a new mission.
> Delete this note block.

**Mission ID:** MISSION-XX  
**Status:** Open  
**Difficulty:** [Low / Medium]  
**Estimated time:** [e.g., 30 minutes]  
**Public information only:** Yes  

---

## Purpose

[One paragraph. State what this mission produces and why it is useful.
Use active voice. 25 words maximum per sentence.]

---

## Inputs

List every public source the contributor must read.

| Source | Type | URL or path |
|---|---|---|
| [Name] | [GitHub repo / web page / file] | [URL] |

---

## Steps

Execute every step in order.

1. [Action verb]. [One clear instruction. 20 words maximum.]
2. [Action verb]. [One clear instruction. 20 words maximum.]
3. [Action verb]. [One clear instruction. 20 words maximum.]
4. Record your receipt for each step. Use this format:

```
COMMAND: <exact command>
OUTPUT:  <relevant output>
MACHINE: <machine type or NO_DATA>
DATE:    <ISO 8601 date>
PATH:    <file or URL>
```

---

## Deliverable

Describe the required output exactly.

- **Format:** [Markdown table / numbered list / file / other]
- **Location:** Place the file at `missions/MISSION-XX/deliverable.md`.
- **Required fields:** [List the required columns or sections.]
- Declare `NO_DATA — reason: <cause>` for every field you cannot measure.

**Example deliverable structure:**

```markdown
# MISSION-XX · Deliverable

## Receipt

COMMAND: ...
OUTPUT:  ...
MACHINE: ...
DATE:    ...
PATH:    ...

## Result

[Table or list here]

## Summary

TOTAL: ...
NO_DATA_COUNT: ...
```

---

## How to verify

Describe how the Sovereign can check the deliverable independently.

1. [Verification step 1.]
2. [Verification step 2.]
3. Confirm that the `NO_DATA` count matches the actual number of missing values.

---

## Restrictions

- Do not modify, push, or delete files in any source repository.
- Do not make network requests beyond those listed in the **Inputs** section.
- Do not reproduce private information, credentials, or internal identifiers.
- Do not invent values. Use `NO_DATA` with a reason when data is missing.

---

## Receipt format reminder

Every step in the deliverable must include a receipt. This is the standard form:

```
COMMAND: <the exact command you ran>
OUTPUT:  <the relevant output lines, truncated to essential content>
MACHINE: <machine name or type, or NO_DATA — reason: not available>
DATE:    <ISO 8601 date>
PATH:    <the file path or URL you inspected>
```

A receipt without all five fields is incomplete.
Declare `NO_DATA — reason: <cause>` for any field you cannot fill.
