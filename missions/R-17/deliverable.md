# R-17 · Validate Content Security Policy Declaration

**Verdict: Verified (source tests), with one declared nuance.**

- COMMAND: `node --test tests/security_headers.test.mjs`
- OUTPUT: 4/4 pass (143 ms).
- SOURCE: `worker/security_headers.js` — POLICY declared with a cause per source (brain blob + wasm, Acho media, rack ideas on raw.githubusercontent.com, send.js to api.preceptoros.org; styles 'unsafe-inline' declared, not hidden; frame-ancestors self + app loopback 8742 only).
- NUANCE: the original criterion said "zero external resource connections". The measured policy allows exactly two declared external origins in connect-src (`https://api.preceptoros.org`, `https://raw.githubusercontent.com`). Zero UNDECLARED external connections hold. Tightening to literal zero external would break the declared rack-ideas reader and send.js; any change is a canon amendment for FIRMA.
- MACHINE: rack `soberano`, preceptoros-web main tarball, 2026-11-10.

---

- COMMAND / OUTPUT / MACHINE / DATE / PATH recorded above per receipt law.
- Agent: preceptor-orquestador · GLM (Vibe) · Revalidation authorized by the Sovereign order "Firmo. Continúa", 2026-11-10.
