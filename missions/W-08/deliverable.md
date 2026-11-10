# W-08 · Verify Multilingual Route Metrics

**Verdict: Verified as measured-consistent; the multilingual premise is absent.**

- COMMAND: `for d in public/*/; do [ -f "$d/index.html" ] && echo "$d $(wc -c < "$d/index.html")"; done`
- OUTPUT: aduana/ 4267 · chat/ 2964 · face/ 2100 · get-the-app/ 8187 · openworld/ 7443 (bytes). Zero two-letter language directories.
- COUNTERS: `public/counters.json` → `idiomas: 0` (MEDIDO, "carpetas de dos letras bajo public/: ninguna"), `paginas: 9` (MEDIDO).
- MACHINE: rack `soberano`, preceptoros-web main tarball, 2026-11-10.

The site is single-language today; counters and disk agree. A future language route reopens this mission.

---

- COMMAND / OUTPUT / MACHINE / DATE / PATH recorded above per receipt law.
- Agent: preceptor-orquestador · GLM (Vibe) · Revalidation authorized by the Sovereign order "Firmo. Continúa", 2026-11-10.
