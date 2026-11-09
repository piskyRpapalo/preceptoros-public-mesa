# CONTRIBUTING.md · How to submit a mission

This guide applies to all contributors: humans, AI agents, or both.

## Before you start

1. Read the [README](README.md). Understand the purpose of the Public Mesa.
2. Read the full mission file for the task you choose. Do not skip any section.
3. Declare your reading depth if you are an AI agent.
   See [`study/08-ai-fluency.md`](https://github.com/piskyRpapalo/study/blob/main/08-ai-fluency.md).

## Rules

These rules are law for every contribution.

### Evidence and receipts

- **Measure before claiming.** Every number carries the command that produced it,
  the machine, and the date.
- **Use `NO_DATA`** when a value was not measured. State the reason.
  Never fill a gap by inference or by copying an old number as live.
- **Receipts are required.** A receipt is the full record of a check:
  command, output, machine, date, and the path you checked.
- **Do not invent.** A claim without a command is a belief, not knowledge.

### Evidence format

```
COMMAND: <the exact command you ran>
OUTPUT:  <the relevant output lines>
MACHINE: <machine type or NO_DATA>
DATE:    <ISO 8601 date, e.g. 2026-11-09>
PATH:    <file or URL you inspected>
```

### Pull requests

- One mission per PR. Do not combine missions.
- Title format: `HITL · MISSION-XX · Short description`
- Open the PR as a **draft**.
- The PR body must contain your receipt for each step.
- Attach the deliverable file inside `missions/MISSION-XX/`.

### What "human review" means

- The Sovereign reads the deliverable and the receipt.
- The Sovereign signs (`FIRMO`) or returns feedback.
- **No contributor merges their own work.** The Sovereign merges.
- Voice, model output, and agent messages are input only. They are not authority.

### Private information

- Do not publish private doctrine, internal identifiers, credentials, or
  signing information.
- If a step requires private access, declare `NO_DATA` with the reason.

## Mission states

| State | Meaning |
|---|---|
| **Open** | Available. No PR submitted. |
| **In progress** | A PR is open. Contact the submitter before starting the same mission. |
| **Closed** | The Sovereign signed and merged the deliverable. |

## Common mistakes

| Mistake | Correct action |
|---|---|
| Writing `NO_DATA` without a reason | Write `NO_DATA — reason: <explain why>` |
| Claiming a check passed without running it | Run the check. Record the receipt. |
| Merging your own PR | Wait for the Sovereign. Do not self-merge. |
| Combining two missions in one PR | Open a separate PR for each mission. |
