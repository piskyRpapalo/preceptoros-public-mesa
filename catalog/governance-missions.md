# Lexicon, Study, and Governance Missions

This catalog file specifies public missions for governance, terminology, and study repositories.
All tasks produce documentation, audit reports, or formal contract specifications.

---

## O-01
- **Title:** Draft Public Contributor Contract for Babel Lexicon
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:64`
- **Problem:** The lexicon repository regulates shared terminology without an explicit agent contract.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Technical writing, governance modeling, ASD-STE100.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Proposed `AGENTS.md` file for public lexicon repository. Location: `missions/O-01/deliverable.md`.
- **Acceptance Criteria:** Define allowed agent actions, receipts, and human-in-the-loop review boundaries.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## O-05
- **Title:** Anchor Directory Names in Public Lexicon
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:72`
- **Problem:** Repository directory names lack formal definitions in the public lexicon.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Markdown, terminology cross-referencing.
- **Dependencies:** `O-01`.
- **Verified Status:** Open.
- **Deliverable:** Cross-reference table linking directory names to lexicon definitions. Location: `missions/O-05/deliverable.md`.
- **Acceptance Criteria:** Every public directory name mapped to an approved term.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## O-06
- **Title:** Define Scope Boundary for Disagreements Document
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:74`
- **Problem:** `DISAGREEMENTS.md` lacks an explicit boundary statement defining its legal scope within the ecosystem.
- **Difficulty:** Low (D1). Estimated time: 45 minutes.
- **Required Skills:** Technical writing, policy drafting.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Scope declaration header for `study/DISAGREEMENTS.md`. Location: `missions/O-06/deliverable.md`.
- **Acceptance Criteria:** Add explicit scope statement defining disagreement arbitration rules.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## L-01
- **Title:** Verify Benchmark Families Documentation
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:86` / `study/14-bench-families.md`
- **Problem:** The benchmark families document lists categories without measured local rows.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Markdown, benchmark auditing.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Updated benchmark table with verified measurements or `NO_DATA` declarations. Location: `missions/L-01/deliverable.md`.
- **Acceptance Criteria:** Every unmeasured benchmark row carries `NO_DATA` with concrete cause.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## N-01
- **Title:** Standardize Mission Field Structure
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:90`
- **Problem:** Canonical mission records lack uniform field names and data types.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Data modeling, ASD-STE100 principles.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Standardized mission schema and validation rules. Location: `missions/N-01/deliverable.md`.
- **Acceptance Criteria:** Verify that all mission entries contain the eleven mandatory fields.
- **Limits:** Propose schema. Do not renumber existing IDs.
- **Human Review:** Sovereign review required.

---

## N-02
- **Title:** Map Mission Dependency Graph
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:92`
- **Problem:** Mission prerequisites are declared in isolation without a navigable visual graph.
- **Difficulty:** High (D3). Estimated time: 3 hours.
- **Required Skills:** Graph visualization, Mermaid syntax, JSON structure.
- **Dependencies:** `N-01`.
- **Verified Status:** Open.
- **Deliverable:** Dependency matrix and static Mermaid diagram of public mission chains. Location: `missions/N-02/deliverable.md`.
- **Acceptance Criteria:** Graph includes all public missions and their explicit blockers.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## N-03
- **Title:** Integrate Unified Documentation Audit Gate
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:94`
- **Problem:** Link checks, language metrics, index freshness, and stale claim audits run in disconnected scripts.
- **Difficulty:** High (D3). Estimated time: 3 hours.
- **Required Skills:** Bash or Node.js scripting, CI design principles.
- **Dependencies:** `W-07`, `W-08`, `W-09`, `W-10`.
- **Verified Status:** Open.
- **Deliverable:** Unified audit script producing a single consolidated markdown receipt. Location: `missions/N-03/deliverable.md`.
- **Acceptance Criteria:** Script executes four sub-checks and reports consolidated status table.
- **Limits:** Read-only execution in sandbox.
- **Human Review:** Sovereign review required.

---

## N-04
- **Title:** Calculate Automated Staleness from Receipts
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:96`
- **Problem:** Staleness tagging is performed manually rather than computed from receipt timestamps.
- **Difficulty:** Medium (D3). Estimated time: 2 hours.
- **Required Skills:** Shell scripting, date arithmetic.
- **Dependencies:** `N-03`.
- **Verified Status:** Open.
- **Deliverable:** Deterministic script computing claim age against system time. Location: `missions/N-04/deliverable.md`.
- **Acceptance Criteria:** Age greater than 30 days automatically triggers `STALE` warning.
- **Limits:** Read-only inspection.
- **Human Review:** Sovereign review required.

---

## R-11
- **Title:** Calibrate Depth Budget by Reader Type
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:126` / `study/08-ai-fluency.md`
- **Problem:** AI reading budgets are static and do not adapt to different model context windows.
- **Difficulty:** High (D3). Estimated time: 3 hours.
- **Required Skills:** AI context modeling, technical specification writing.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Reading depth calibration table for small, medium, and large context windows. Location: `missions/R-11/deliverable.md`.
- **Acceptance Criteria:** Token ceilings and file depths specified for five reading levels.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## R-17
- **Title:** Validate Content Security Policy Declaration
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:138`
- **Problem:** Frontend Content Security Policy (CSP) is implicit and requires formal declaration.
- **Difficulty:** Low (D1). Estimated time: 1 hour.
- **Required Skills:** HTTP security headers, web testing.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** CSP audit table verifying zero external connection directives. Location: `missions/R-17/deliverable.md`.
- **Acceptance Criteria:** Confirm that CSP header prohibits external scripts, styles, and telemetry.
- **Limits:** Read-only header check.
- **Human Review:** Sovereign review required.

---

## R-23
- **Title:** Document Public Disagreement Resolution Protocol
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:150` / `study/DISAGREEMENTS.md`
- **Problem:** Conflict resolution process between contributing AI agents lacks public documentation.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Governance writing, dispute resolution modeling.
- **Dependencies:** `O-06`.
- **Verified Status:** Open.
- **Deliverable:** Proposed section in `study/DISAGREEMENTS.md` for agent-to-agent conflicts. Location: `missions/R-23/deliverable.md`.
- **Acceptance Criteria:** Define evidence-based dispute resolution with Sovereign final arbitration.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.
