# Frontend, Interaction, and Canon Missions

This catalog file specifies public missions for front-end architecture, UI optimization, and accessibility.
All tasks focus on user experience, design consistency, and screen reader compatibility.

---

## G4
- **Title:** Add Measured Front-End CSS Optimizations
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:185`
- **Problem:** Public web application lacks measured CSS enhancements: `text-wrap`, `scrollbar-gutter`, and `view-transitions`.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Modern CSS, browser rendering benchmarks.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Proposal PR adding measured CSS properties with before-and-after performance receipts. Location: `missions/G4/deliverable.md`.
- **Acceptance Criteria:** Verify zero layout breaks. Test across standard viewports.
- **Limits:** CSS styling only. Do not alter DOM logic or state contracts.
- **Human Review:** Sovereign review required.

---

## F7
- **Title:** Verify Public Web Accessibility Standards (EN 301 549)
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:173`
- **Problem:** Web UI requires verification against EN 301 549 (44px touch targets, contrast, screen reader labels).
- **Difficulty:** High (D3). Estimated time: 3 hours.
- **Required Skills:** Accessibility auditing, WCAG/EN 301 549 standards.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Comprehensive accessibility audit report with verifiable test matrix. Location: `missions/F7/deliverable.md`.
- **Acceptance Criteria:** Measure all interactive targets. Document missing audio/aria labels as `NO_DATA`.
- **Limits:** Read-only audit.
- **Human Review:** Sovereign review required.

---

## D10
- **Title:** Specify Audio Mode Interaction for Screenless Use
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:151`
- **Problem:** Screenless interaction specification requires local TTS integration and voice privacy declaration.
- **Difficulty:** High (D3). Estimated time: 3 hours.
- **Required Skills:** Audio synthesis specification, technical design.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Specification document defining zero-network audio interface requirements. Location: `missions/D10/deliverable.md`.
- **Acceptance Criteria:** State exact requirements: local TTS only, zero microphone streaming to third parties.
- **Limits:** Specification only.
- **Human Review:** Sovereign review required.

---

## A7
- **Title:** Verify Read-Only Public GitHub Reader Integration
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:113`
- **Problem:** Public repository data access must use unauthenticated GET requests without API secrets.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** Git, GitHub REST API, testing.
- **Dependencies:** None.
- **Verified Status:** Verified.
- **Deliverable:** Verification report confirming read-only test suite passes without credentials. Location: `missions/A7/deliverable.md`.
- **Acceptance Criteria:** Green test run verified on public API endpoints with zero stored tokens.
- **Limits:** Read-only.
- **Human Review:** Verified by Sovereign in previous session.

---

## I2
- **Title:** Document Ephemeral Visitor Needs on Frontend
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:204`
- **Problem:** The frontend needs an explicit requirements document for first-time visitors without persistent accounts.
- **Difficulty:** Low (D1). Estimated time: 1 hour.
- **Required Skills:** User requirements analysis, technical writing.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Requirements document detailing visitor onboarding and ephemeral state lifecycle. Location: `missions/I2/deliverable.md`.
- **Acceptance Criteria:** List all controls available to an unauthenticated visitor.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## I6
- **Title:** Specify Separation of Communications Panels
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:208`
- **Problem:** Radio, chat, and system updates share combined panels, causing visual congestion.
- **Difficulty:** Medium (D2). Estimated time: 2 hours.
- **Required Skills:** UI specification, modular design.
- **Dependencies:** `I2`.
- **Verified Status:** Open.
- **Deliverable:** Architectural layout specification separating Radio, Chat, and Echoes panels. Location: `missions/I6/deliverable.md`.
- **Acceptance Criteria:** Define independent layout boxes, keybindings, and accessibility labels.
- **Limits:** Specification only.
- **Human Review:** Sovereign review required.

---

## I7
- **Title:** Audit and Remove Broken Links in Web Panels
- **Source:** `preceptoros-web/docs/canon-map-details-20261107.md:209`
- **Problem:** Web panels contain obsolete text links that return 404 errors.
- **Difficulty:** Low (D1). Estimated time: 1 hour.
- **Required Skills:** Web inspection, Markdown.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Audit table of dead links in panel components with proposed cleanup diff. Location: `missions/I7/deliverable.md`.
- **Acceptance Criteria:** Every link in panel templates tested. Stale references removed.
- **Limits:** Propose diff. Do not alter panel state logic.
- **Human Review:** Sovereign review required.
