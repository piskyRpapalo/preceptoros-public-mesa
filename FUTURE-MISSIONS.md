# Future missions · Public Mesa

**Effective date:** 2026-11-10 · **Sovereign direction:** all future missions live in the two Mesa repositories. This is the **public** intake route for humans and AI preceptors.

## Choose or propose public work here

- Start with the [existing public catalog](CATALOG.md) and its [machine-readable draft](catalog.json). It holds 29 staged entries with dated, not necessarily current, status claims. Before selecting an entry, check its source, existing PRs and whether code already landed.
- **New public mission:** open an Issue **in this Public Mesa**, not in WEB, APP, LAB or STUDY, with a source link, original ID, objective, testable result and any `NO_DATA` cause. Reuse an existing issue when the same mission exists.
- **Uncertain or restricted mission:** route for private review, not here. Never paste private source text, tokens, device identifiers or credentials in public issues.
- **Implementation:** submit a PR to the relevant software/ground-truth repository and link the Public Mesa mission. Code, tests and measured evidence belong to the code repository; assignment and future-work status belong here.
- **Human review:** the Sovereign signs software changes. A preceptor may propose and test but cannot give its own signature.

## One home, many references

This Public Mesa is the unique active task home for reviewed public missions. Private Mesa is the unique home for unpublished or sensitive tasks. A mission is **not** OPEN in both places. A private task promoted to the public catalog leaves only a non-operational routing pointer in the private record.

The old [WEB §9 mission map](https://github.com/piskyRpapalo/preceptoros-web/blob/main/docs/canon-map-details-20261107.md), [GEN3 proposals](https://github.com/piskyRpapalo/preceptoros-web/blob/main/docs/misiones-compacta-20261108.md), code-owner `odd/tasks/` and older Roadmap documents remain dated historical evidence. **No new future mission lists** will be created in those repositories.

## Required fields for a new public mission

`ID`, `SOURCE (repo@SHA:path#original-ID)`, `TITLE`, `OWNER_REPO`, `DEPENDENCIES`, `STATE`, `MEASURE`, `NO_DATA_CAUSE`, `RELATED_PR`, `NEXT_STEP`, `LAST_VERIFIED`.

Use states `PROPOSED`, `OPEN`, `TAKEN`, `VERIFIED`, `DONE` or `NO_DATA`; never infer `DONE` from a test fixture or `LIVE` from a file's presence. For voice and screen-reader support, the same state must be available as readable text and machine data; a running speech bridge is **NO_DATA** until verified.

## Current boundary

**Policy:** new public mission intake is here as directed.  
**History:** existing catalog files are not deleted or silently reclassified.  
**Completion:** full migration of legacy 78 A–I, N1–N14, GEN3 60, Y1–Y12 and Roadmap M1–M8 remains `NO_DATA` until source-by-source reconciliation. No claim of an automated sync, user-interface integration or deployment.

Codex · GPT-6 · 2026-11-10. Documentation-only receipt. The Sovereign keeps all consequential decisions.
