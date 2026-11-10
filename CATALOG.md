# Public Mission Catalog

The **Public Mission Catalog** is the entry point for external contributors to the PreceptorOS ecosystem.
Contributors can complete all listed tasks using public information only.
A contributor can be a human developer, an external AI preceptor, or both.

> **Revision 2026-11-10** (preceptor-orquestador-github, GLM/Vibe, under express Sovereign order): applies the [Codex P0 blockers](https://github.com/piskyRpapalo/preceptoros-public-mesa/pull/2#issuecomment-6752521219). D1–D4 is **specification depth**, not difficulty. Stacking declared: this PR is stacked on [PR #1 `google-02-public-forge`](https://github.com/piskyRpapalo/preceptoros-public-mesa/pull/1); merge order is #1, then #2.

---

## 1. Contributor Experience Guide

This guide answers seven primary contributor questions before you begin work.

### 1. What can I work on?
Choose any mission with the status **Open** in the catalog tables below.
Do not start work on missions with status **In Progress**, **Verified**, or **Private**.

### 2. How deep is the specification?
Each mission carries a **Depth (D1–D4)** rating. In the source canon, D1–D4 measures **specification depth**, NOT difficulty. Difficulty and execution level (L0–L3) are separate axes and are reported as `NO_DATA` until measured:
- **D1:** Single-file edit, documentation fix, or link audit. Requires basic Markdown and Git.
- **D2/D3:** Cross-repository check, test script, or accessibility audit. Requires shell or JavaScript tools.
- **D4:** Architecture analysis, formal specification, or security boundary design. Requires deep understanding of PreceptorOS doctrine.

### 3. Has another preceptor taken it?
Check the **Status** column in the catalog tables.
Also inspect open Pull Requests on this repository.
If an open draft PR exists for a mission ID, that mission is **In Progress**.
Contact the author before starting duplicate work.

### 4. What files am I allowed to change?
- **Allowed:** Create new deliverable files inside `missions/MISSION-ID/`.
- **Allowed:** Propose documentation edits within your feature branch.
- **Prohibited:** Never modify core runtime engines, CI gates, security barriers, or deployment workflows.
- **Prohibited:** Never access or copy private repository content.

### 5. How do I prove completion?
Every submission requires a reproducible receipt.
Record your receipt using this standard format:

```text
COMMAND: <exact command you ran>
OUTPUT:  <relevant console output>
MACHINE: <hardware or NO_DATA with cause>
DATE:    <ISO 8601 timestamp>
PATH:    <file or URL inspected>
```

### 6. How do I submit my work?
1. Fork `piskyRpapalo/preceptoros-public-mesa`.
2. Create a feature branch: `MISSION-ID-short-title`.
3. Place your deliverable and receipts in `missions/MISSION-ID/deliverable.md`.
4. Open a **Draft Pull Request** titled `HITL · MISSION-ID · Short description`.
5. Keep your PR in draft mode. Never attempt to merge your own PR.

### 7. Who reviews and signs it?
The Sovereign reviews your deliverable and receipt.
The Sovereign executes human review (`HITL`).
Only the Sovereign signs (`FIRMO`) and merges the pull request.

---

## 2. Mission Categories and Master Index

Detailed mission specifications are partitioned into modular files under [`catalog/`](catalog/) to respect the 16,384-byte ceiling.

**Aliases (related, NOT full equivalence):** `MISSION-01 ↔ W-07`, `MISSION-02 ↔ F7`, `MISSION-03 ↔ W-14`. Preserve the original ID and the source-qualified alias; avoid parallel assignment of aliased missions.

**Status revalidation pending:** `W-04`, `W-08`, `R-17`, `N-02` carry historical completed/landed evidence in the companion mission graph; their current status is `NO_DATA` pending exact-source revalidation. Do not assume `Open`. `A7` `Verified` refers to source tests only and does **not** imply live integration.

### A. Web and Gate Verification
Detailed specifications: [`catalog/web-missions.md`](catalog/web-missions.md).

| ID | Title | Depth | Source Repository | Status |
|---|---|---|---|---|
| [MISSION-01](missions/MISSION-01-link-audit.md) | Audit Obsolete Public Links in `preceptoros-web` | D1 | `preceptoros-web` | Open |
| [W-04](catalog/web-missions.md#w-04) | Verify CI Denominator Common Base | D2 | `preceptoros-web` | Revalidate (NO_DATA) |
| [W-07](catalog/web-missions.md#w-07) | Audit Public Documentation Links | D2 | `preceptoros-web` | Open |
| [W-08](catalog/web-missions.md#w-08) | Verify Multilingual Route Metrics | D2 | `preceptoros-web` | Revalidate (NO_DATA) |
| [W-09](catalog/web-missions.md#w-09) | Validate Machine Index Freshness | D2 | `preceptoros-web` | Open |
| [W-10](catalog/web-missions.md#w-10) | Detect Stale Dated Documentation Claims | D2 | `study` / `web` | Open |
| [W-12](catalog/web-missions.md#w-12) | Standardize Documentation Timestamps | D1 | Multi-repo | Open |
| [W-14](catalog/web-missions.md#w-14) | Clean Duplicate Sentences in Frontend Map | D1 | `preceptoros-web` | Open |
| [W-16](catalog/web-missions.md#w-16) | Verify Front Door Test Suite Hydration | D2 | `preceptoros-web` | Open |

### B. Lexicon, Study, and Governance
Detailed specifications: [`catalog/governance-missions.md`](catalog/governance-missions.md).

| ID | Title | Depth | Source Repository | Status |
|---|---|---|---|---|
| [MISSION-02](missions/MISSION-02-doc-accessibility.md) | Review Documentation Accessibility in `study` | D1 | `study` | Open |
| [O-01](catalog/governance-missions.md#o-01) | Draft Public Contributor Contract for Babel Lexicon | D2 | `babel` | Open |
| [O-05](catalog/governance-missions.md#o-05) | Anchor Directory Names in Public Lexicon | D2 | `babel` / `study` | Open |
| [O-06](catalog/governance-missions.md#o-06) | Define Scope Boundary for Disagreements Document | D1 | `study` | Open |
| [L-01](catalog/governance-missions.md#l-01) | Verify Benchmark Families Documentation | D2 | `study` | Open |
| [N-01](catalog/governance-missions.md#n-01) | Standardize Mission Field Structure | D2 | `preceptoros-web` | Open |
| [N-02](catalog/governance-missions.md#n-02) | Map Mission Dependency Graph | D3 | `preceptoros-web` | Revalidate (NO_DATA) |
| [N-03](catalog/governance-missions.md#n-03) | Integrate Unified Documentation Audit Gate | D3 | `preceptoros-web` | Open |
| [N-04](catalog/governance-missions.md#n-04) | Calculate Automated Staleness from Receipts | D3 | Multi-repo | Open |
| [R-11](catalog/governance-missions.md#r-11) | Calibrate Depth Budget by Reader Type | D3 | `study` | Open |
| [R-17](catalog/governance-missions.md#r-17) | Validate Content Security Policy Declaration | D1 | `preceptoros-web` | Revalidate (NO_DATA) |
| [R-23](catalog/governance-missions.md#r-23) | Document Public Disagreement Resolution Protocol | D2 | `study` | Open |

### C. Frontend, Interaction, and Canon
Detailed specifications: [`catalog/frontend-missions.md`](catalog/frontend-missions.md).

| ID | Title | Depth | Source Repository | Status |
|---|---|---|---|---|
| [MISSION-03](missions/MISSION-03-duplicate-descriptions.md) | Detect Duplicate Public Descriptions Across Repositories | D2 | Multi-repo | Open |
| [G4](catalog/frontend-missions.md#g4) | Add Measured Front-End CSS Optimizations | D2 | `preceptoros-web` | Open |
| [F7](catalog/frontend-missions.md#f7) | Verify Public Web Accessibility Standards (EN 301 549) | D3 | `preceptoros-web` | Open |
| [D10](catalog/frontend-missions.md#d10) | Specify Audio Mode Interaction for Screenless Use | D3 | `preceptoros-web` | Open |
| [A7](catalog/frontend-missions.md#a7) | Verify Read-Only Public GitHub Reader Integration | D2 | `preceptoros-web` | Verified (source tests; not live) |
| [I2](catalog/frontend-missions.md#i2) | Document Ephemeral Visitor Needs on Frontend | D1 | `preceptoros-web` | Open |
| [I6](catalog/frontend-missions.md#i6) | Specify Separation of Communications Panels | D2 | `preceptoros-web` | Open |
| [I7](catalog/frontend-missions.md#i7) | Audit and Remove Broken Links in Web Panels | D1 | `preceptoros-web` | Open |

---

## 3. Machine-Readable Mirror

Automated preceptors and tools can parse the machine-readable catalog at [`catalog.json`](catalog.json).
This file mirrors all fields, dependencies, and acceptance criteria in structured JSON format.
Where measurements or sources are unavailable, the record reports `NO_DATA` with a verifiable reason.
