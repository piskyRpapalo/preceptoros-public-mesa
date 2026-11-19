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

## A2A collaboration contract (only when other agents or nodes participate)

A mission is **not** a permission grant. Fill these fields before proposing an A2A handoff, or state `NO_DATA — reason: <cause>`. No missing field may authorize a transfer.

| Required declaration | Value or grounded NO_DATA |
|---|---|
| Sending person/node and receiving person/node | [Public aliases; never private addresses or credentials] |
| Proposed agent role and requested capability | [One bounded purpose; a public agent card grants nothing] |
| Input and output Acho schema/version | [Public paths; strict UTF-8] |
| Control-message ceiling | [At most 1,023 bytes; actual measurement command, machine and date] |
| Separate data budget, if needed | [Maximum bytes, format and checksum; 25 MiB is a ceiling, not proof of live upload] |
| Time budget | [Maximum `timeout_ms`, measurement or NO_DATA with cause] |
| Physical resource budget | [Measured watts/energy with method and date, or NO_DATA with cause] |
| Licence and source provenance | [SPDX identifier and permitted reuse; cite original authors] |
| Privacy inspection | [Command, tool/version, outcome and date; never hard-code a PII-free claim] |
| Human consent and revocation | [Sender approves exact emission; receiver approves exact acceptance; both may refuse] |
| Evidence and state | [Receipt digest, measured result, or NO_DATA(cause); no fabricated LIVE] |

**Fail-closed checks:** A missing consent, unspecified budget, unsupported schema, stale grant, absent provenance or unmeasured destination prevents an A2A transfer. Agents can prepare proposals and public receipts; they cannot self-sign, access private databases or initiate remote services. Public GitHub carries only expressly approved declarations, never private corpora. Record failures as `NO_DATA` with the concrete cause, and continue unrelated authorized work.

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
