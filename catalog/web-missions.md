# Web and Gate Verification Missions

This catalog file specifies public missions for `preceptoros-web` and gate testing.
All operations are read-only or propose-only within contributor feature branches.

---

## W-04
- **Title:** Verify CI Denominator Common Base
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:34`
- **Problem:** Test suites execute without a verified common denominator. CI can silence a failing suite without detection.
- **Difficulty:** Medium. Estimated time: 2 hours.
- **Required Skills:** GitHub Actions workflow syntax, Node.js test runners.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Audit table comparing declared test suites in `gate.yml` against actual test files. Location: `missions/W-04/deliverable.md`.
- **Acceptance Criteria:** Total suite count verified. Every missing test file documented as `NO_DATA` with cause.
- **Limits:** Do not modify `.github/workflows/gate.yml` directly. Propose-only.
- **Human Review:** Sovereign signs (`FIRMO`) before any workflow change.

---

## W-07
- **Title:** Audit Public Documentation Links
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:40`
- **Problem:** URLs in public READMEs, `llms.txt`, and `METHOD.md` can break over time without warning.
- **Difficulty:** Low. Estimated time: 1 hour.
- **Required Skills:** Bash scripting, curl, HTTP response interpretation.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Link verification script and status table. Location: `missions/W-07/deliverable.md`.
- **Acceptance Criteria:** Check HTTP status for all cited external and internal links. Record 404 and 301 responses.
- **Limits:** Read-only inspection. No network requests outside declared sources.
- **Human Review:** Sovereign review required.

---

## W-08
- **Title:** Verify Multilingual Route Metrics
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:42`
- **Problem:** Landing page claims nine languages, but language routes require verifiable byte metrics.
- **Difficulty:** Medium. Estimated time: 2 hours.
- **Required Skills:** Node.js file inspection, metrics calculation.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Byte and route inventory table per language. Location: `missions/W-08/deliverable.md`.
- **Acceptance Criteria:** Measure file size and route paths for every language directory. Compare against `counters.json`.
- **Limits:** Read-only inspection. Propose metric inclusion without modifying routing logic.
- **Human Review:** Sovereign review required.

---

## W-09
- **Title:** Validate Machine Index Freshness
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:44`
- **Problem:** Machine-readable index `ai-index.json` can become stale relative to repository trees.
- **Difficulty:** Medium. Estimated time: 2 hours.
- **Required Skills:** JSON parsing, Git tree comparison.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Comparison report between `ai-index.json` entries and repository files. Location: `missions/W-09/deliverable.md`.
- **Acceptance Criteria:** Detect all added, moved, or deleted files missing from `ai-index.json`.
- **Limits:** Read-only inspection.
- **Human Review:** Sovereign review required.

---

## W-10
- **Title:** Detect Stale Dated Documentation Claims
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:46`
- **Problem:** Dated performance and architectural claims age beyond 30 days without re-verification.
- **Difficulty:** Low. Estimated time: 1 hour.
- **Required Skills:** Python or Bash, regex, date parsing.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Inventory table of all dated claims older than 30 days. Location: `missions/W-10/deliverable.md`.
- **Acceptance Criteria:** Flag all statements with timestamps older than 30 days as `STALE`.
- **Limits:** Read-only inspection.
- **Human Review:** Sovereign review required.

---

## W-12
- **Title:** Standardize Documentation Timestamps
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:50`
- **Problem:** Status boards without explicit timestamps prevent temporal auditability.
- **Difficulty:** Low. Estimated time: 30 minutes.
- **Required Skills:** Markdown formatting, ISO 8601 syntax.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** PR adding standard ISO 8601 timestamp headers to untimed status documents.
- **Acceptance Criteria:** Every status doc has an unambiguous date header.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## W-14
- **Title:** Clean Duplicate Sentences in Frontend Map
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:54`
- **Problem:** The frontend web map repeats sentences already declared in prior sections.
- **Difficulty:** Low. Estimated time: 45 minutes.
- **Required Skills:** Text analysis, Markdown editing, ASD-STE100 principles.
- **Dependencies:** None.
- **Verified Status:** Open.
- **Deliverable:** Diff proposal removing redundant phrases from public web map documentation.
- **Acceptance Criteria:** Zero semantic loss. Identical duplicate phrases removed.
- **Limits:** Documentation only.
- **Human Review:** Sovereign review required.

---

## W-16
- **Title:** Verify Front Door Test Suite Hydration
- **Source:** `preceptoros-web/docs/misiones-compacta-20261108.md:58`
- **Problem:** Front door test suites can lose test case coverage during rapid component changes.
- **Difficulty:** Medium. Estimated time: 2 hours.
- **Required Skills:** Node.js, JavaScript test execution.
- **Dependencies:** `W-04`.
- **Verified Status:** Open.
- **Deliverable:** Test execution log and hydration report. Location: `missions/W-16/deliverable.md`.
- **Acceptance Criteria:** All test cases in `front_door_cases.mjs` pass with verified receipt.
- **Limits:** Test files only. No runtime modifications.
- **Human Review:** Sovereign review required.
