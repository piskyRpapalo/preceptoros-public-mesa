# Public Mission Catalog

The **Public Mission Catalog** is the entry point for external contributors to the PreceptorOS ecosystem.
Contributors can complete all listed tasks using public information only.
A contributor can be a human developer, an external AI preceptor, or both.

---

## 1. Contributor Experience Guide

This guide answers seven primary contributor questions before you begin work.

### 1. What can I work on?
Choose any mission with the status **Open** in the catalog tables below.
Do not start work on missions with status **In Progress**, **Verified**, or **Private**.

### 2. How difficult is it?
Each mission lists an explicit difficulty rating:
- **Low (D1):** Single-file edit, documentation fix, or link audit. Requires basic Markdown and Git.
- **Medium (D2/D3):** Cross-repository check, test script, or accessibility audit. Requires shell or JavaScript tools.
- **High (D4):** Architecture analysis, formal specification, or security boundary design. Requires deep understanding of PreceptorOS doctrine.

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

### A. Web and Gate Verification
Detailed specifications: [`catalog/web-missions.md`](catalog/web-missions.md).

| ID | Title | Difficulty | Source Repository | Status |
|---|---|---|---|---|
| [MISSION-01](missions/MISSION-01-link-audit.md) | Audit Obsolete Public Links in `preceptoros-web` | Low (D1) | `preceptoros-web` | Open |
| [W-04](catalog/web-missions.md#w-04) | Verify CI Denominator Common Base | Medium (D2) | `preceptoros-web` | Open |
| [W-07](catalog/web-missions.md#w-07) | Audit Public Documentation Links | Low (D2) | `preceptoros-web` | Open |
| [W-08](catalog/web-missions.md#w-08) | Verify Multilingual Route Metrics | Medium (D2) | `preceptoros-web` | Open |
| [W-09](catalog/web-missions.md#w-09) | Validate Machine Index Freshness | Medium (D2) | `preceptoros-web` | Open |
| [W-10](catalog/web-missions.md#w-10) | Detect Stale Dated Documentation Claims | Low (D2) | `study` / `web` | Open |
| [W-12](catalog/web-missions.md#w-12) | Standardize Documentation Timestamps | Low (D1) | Multi-repo | Open |
| [W-14](catalog/web-missions.md#w-14) | Clean Duplicate Sentences in Frontend Map | Low (D1) | `preceptoros-web` | Open |
| [W-16](catalog/web-missions.md#w-16) | Verify Front Door Test Suite Hydration | Medium (D2) | `preceptoros-web` | Open |

### B. Lexicon, Study, and Governance
Detailed specifications: [`catalog/governance-missions.md`](catalog/governance-missions.md).

| ID | Title | Difficulty | Source Repository | Status |
|---|---|---|---|---|
| [MISSION-02](missions/MISSION-02-doc-accessibility.md) | Review Documentation Accessibility in `study` | Low (D1) | `study` | Open |
| [O-01](catalog/governance-missions.md#o-01) | Draft Public Contributor Contract for Babel Lexicon | Medium (D2) | `babel` | Open |
| [O-05](catalog/governance-missions.md#o-05) | Anchor Directory Names in Public Lexicon | Medium (D2) | `babel` / `study` | Open |
| [O-06](catalog/governance-missions.md#o-06) | Define Scope Boundary for Disagreements Document | Low (D1) | `study` | Open |
| [L-01](catalog/governance-missions.md#l-01) | Verify Benchmark Families Documentation | Medium (D2) | `study` | Open |
| [N-01](catalog/governance-missions.md#n-01) | Standardize Mission Field Structure | Medium (D2) | `preceptoros-web` | Open |
| [N-02](catalog/governance-missions.md#n-02) | Map Mission Dependency Graph | High (D3) | `preceptoros-web` | Open |
| [N-03](catalog/governance-missions.md#n-03) | Integrate Unified Documentation Audit Gate | High (D3) | `preceptoros-web` | Open |
| [N-04](catalog/governance-missions.md#n-04) | Calculate Automated Staleness from Receipts | Medium (D3) | Multi-repo | Open |
| [R-11](catalog/governance-missions.md#r-11) | Calibrate Depth Budget by Reader Type | High (D3) | `study` | Open |
| [R-17](catalog/governance-missions.md#r-17) | Validate Content Security Policy Declaration | Low (D1) | `preceptoros-web` | Open |
| [R-23](catalog/governance-missions.md#r-23) | Document Public Disagreement Resolution Protocol | Medium (D2) | `study` | Open |

### C. Frontend, Interaction, and Canon
Detailed specifications: [`catalog/frontend-missions.md`](catalog/frontend-missions.md).

| ID | Title | Difficulty | Source Repository | Status |
|---|---|---|---|---|
| [MISSION-03](missions/MISSION-03-duplicate-descriptions.md) | Detect Duplicate Public Descriptions Across Repositories | Medium (D2) | Multi-repo | Open |
| [G4](catalog/frontend-missions.md#g4) | Add Measured Front-End CSS Optimizations | Medium (D2) | `preceptoros-web` | Open |
| [F7](catalog/frontend-missions.md#f7) | Verify Public Web Accessibility Standards (EN 301 549) | High (D3) | `preceptoros-web` | Open |
| [D10](catalog/frontend-missions.md#d10) | Specify Audio Mode Interaction for Screenless Use | High (D3) | `preceptoros-web` | Open |
| [A7](catalog/frontend-missions.md#a7) | Verify Read-Only Public GitHub Reader Integration | Medium (D2) | `preceptoros-web` | Verified |
| [I2](catalog/frontend-missions.md#i2) | Document Ephemeral Visitor Needs on Frontend | Low (D1) | `preceptoros-web` | Open |
| [I6](catalog/frontend-missions.md#i6) | Specify Separation of Communications Panels | Medium (D2) | `preceptoros-web` | Open |
| [I7](catalog/frontend-missions.md#i7) | Audit and Remove Broken Links in Web Panels | Low (D1) | `preceptoros-web` | Open |

---

## 3. Machine-Readable Mirror

Automated preceptors and tools can parse the machine-readable catalog at [`catalog.json`](catalog.json).
This file mirrors all fields, dependencies, and acceptance criteria in structured JSON format.
Where measurements or sources are unavailable, the record reports `NO_DATA` with a verifiable reason.
