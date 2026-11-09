# preceptoros-public-mesa

The **Public Mesa** is the mission catalogue for external contributors.
It lists tasks that any contributor can complete using public information only.
A contributor may be a human, an AI agent, or both working together.

## What this repository is

The Public Mesa is one part of the **PreceptorOS** ecosystem:

| Repository | Role |
|---|---|
| [`preceptoros-web`](https://github.com/piskyRpapalo/preceptoros-web) | Public gateway — zero-external-request frontend |
| [`preceptoros-app`](https://github.com/piskyRpapalo/preceptoros-app) | Companion app — local AI orchestration |
| [`study`](https://github.com/piskyRpapalo/study) | Public doctrine, governance laws, measurement contracts |
| **`preceptoros-public-mesa`** (this repo) | Public mission catalogue for contributors |

**Core principle: silicon proposes, carbon signs.**
An AI agent may prepare, measure, and suggest.
A human signature precedes every consequential action.

## How contributions work

1. Read [CONTRIBUTING.md](CONTRIBUTING.md) before starting.
2. Choose an open mission from the [`missions/`](missions/) directory.
3. Fork this repository.
4. Create a branch named `MISSION-XX-your-short-description`.
5. Complete the mission. Place your deliverable in `missions/MISSION-XX/`.
6. Open a **draft Pull Request** titled `HITL · MISSION-XX · Short description`.
7. The Sovereign reviews the deliverable and signs or returns feedback.
8. The Sovereign merges. No contributor merges their own work.

## Reading depth for AI agents

If you are an AI reading this repository, declare your depth first.
See [`study/08-ai-fluency.md`](https://github.com/piskyRpapalo/study/blob/main/08-ai-fluency.md)
for the five canonical depths and their budgets.
Anything beyond your declared budget is `NO_DATA` with a cause.

## Open missions

| Mission | Title | Status |
|---|---|---|
| [MISSION-01](missions/MISSION-01-link-audit.md) | Audit obsolete public links in `preceptoros-web` | Open |
| [MISSION-02](missions/MISSION-02-doc-accessibility.md) | Review documentation accessibility in `study` | Open |
| [MISSION-03](missions/MISSION-03-duplicate-descriptions.md) | Detect duplicate public descriptions across repositories | Open |

## Key vocabulary

| Term | Meaning |
|---|---|
| **NO\_DATA** | A value was not measured. State the cause. Never invent a value. |
| **Receipt** | A record of a check: the command, machine, date, and result. |
| **Evidence** | A measured fact with a verifiable source. |
| **HITL** | Human-in-the-loop. Required on every PR title. |
| **THE MARCH** | The workflow: Explore → Implement → Check. |
| **Preceptor** | Any agent (human or AI) that reads this world and works under these laws. |

## License

Apache 2.0. See [LICENSE](LICENSE).
