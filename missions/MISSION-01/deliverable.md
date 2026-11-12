# MISSION-01 · Deliverable · Link audit (preceptoros-web root Markdown)

**Agent:** Grokbot · xAI · 2026-11-12  
**Repo audited:** `piskyRpapalo/preceptoros-web` @ clone depth-1 main  
**Scope:** `*.md` at repository root only · no subdirectories · no source edits

---

## Section 1 — Receipts

### Step 1 · Clone

```
COMMAND: git clone --depth 1 https://github.com/piskyRpapalo/preceptoros-web.git
OUTPUT:   Cloning into 'preceptoros-web-m01'... done (1321 files)
MACHINE:  measurement host (public network curl/git)
DATE:     2026-11-12T01:40:00Z
PATH:     /tmp/preceptoros-web-m01
```

### Step 2 · List root Markdown

```
COMMAND: find . -maxdepth 1 -name "*.md" | sort
OUTPUT:
./AGENTS.md
./COMPLIANCE.md
./CONTRIBUTING.md
./DEPLOY.md
./DISAGREEMENTS.md
./EXCEPCIONES.md
./LANGUAGES.md
./LINEA_DEL_TIEMPO.md
./README.md
./SECURITY.md
./THE_WORKSHOP.md
MACHINE: measurement host
DATE:    2026-11-12T01:40:00Z
PATH:    preceptoros-web root
```

### Step 3 · Extract unique URLs

```
COMMAND: python3 regex extract https?:// from each root *.md; dedupe; strip trailing punctuation
OUTPUT:  29 (source_file, URL) pairs · 24 unique URLs
MACHINE: measurement host
DATE:    2026-11-12T01:41:00Z
PATH:    root *.md
```

### Step 4 · HTTP status (sample policy)

```
COMMAND: curl -o /dev/null -s -w "%{http_code}" --max-time 10 -L --max-redirs 1 <URL>
POLICY:  block loopback/private hosts → Status_code NO_DATA (not fetched)
NOTE:    Unauthenticated GitHub often returns 404 for *private* repos; label is measured HTTP code, not proof of deletion.
DATE:    2026-11-12T01:42:00Z
```

---

## Section 2 — Link table

| Source_file | URL | Status_code | Label |
|---|---|---|---|
| AGENTS.md | https://github.com/piskyRpapalo/study/blob/main/08-ai-fluency.md | 200 | OK |
| CONTRIBUTING.md | https://github.com/piskyRpapalo/study/blob/main/08-ai-fluency.md | 200 | OK |
| CONTRIBUTING.md | https://github.com/piskyRpapalo/preceptoros-app | 200 | OK |
| CONTRIBUTING.md | https://github.com/piskyRpapalo/preceptoros-app/blob/main/PRECEPTOR.md | 200 | OK |
| CONTRIBUTING.md | https://github.com/piskyRpapalo/lab | 200 | OK |
| CONTRIBUTING.md | https://github.com/piskyRpapalo/study | 200 | OK |
| CONTRIBUTING.md | https://github.com/piskyRpapalo/study/blob/main/14-bench-families.md | 200 | OK |
| README.md | https://github.com/piskyRpapalo | 200 | OK |
| README.md | https://github.com/piskyRpapalo/study | 200 | OK |
| README.md | https://github.com/piskyRpapalo/study/blob/main/08-ai-fluency.md | 200 | OK |
| README.md | https://github.com/piskyRpapalo/preceptoros-app | 200 | OK |
| README.md | https://github.com/piskyRpapalo/babel | 200 | OK |
| README.md | https://github.com/piskyRpapalo/preceptoros-companion | 200 | OK |
| README.md | https://github.com/piskyRpapalo/lab | 200 | OK |
| README.md | https://github.com/piskyRpapalo/buzon | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/buzon/issues/19 | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/buzon/issues/30 | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/buzon/issues/53 | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/firmas | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/preceptoros-terminal | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/roadmap | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/p0x | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/hexelion-nexo | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/aduana | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/preceptoros-atlas | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/preceptoros-coder | 404 | NOT_FOUND |
| README.md | https://github.com/piskyRpapalo/CineK | 404 | NOT_FOUND |
| README.md | http://127.0.0.1:8000/ | NO_DATA | NO_DATA |
| SECURITY.md | https://api.preceptoros.org/api/v1/cedulas | 200 | OK |

**NO_DATA reason (127.0.0.1):** loopback/local — not fetched (policy: no internal targets).

**Caveat on 404:** Several paths are known-private org repos; GitHub returns 404 without auth. Measured code is still `404`. Sovereign may re-check with authenticated access.

---

## Section 3 — Summary

```
TOTAL_LINKS_CHECKED: 29
BROKEN_OR_OBSOLETE:  14
NO_DATA_COUNT:       1
DATE:                2026-11-12T01:42:00Z
```

BROKEN_OR_OBSOLETE = rows where Label is not `OK` (includes NOT_FOUND and NO_DATA).

**Silicon proposes. The Sovereign signs.**
