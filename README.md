# MeshVault Skills Starter

Free, open agent skills from [MeshVault](https://meshvault.ai?utm_source=github&utm_medium=readme&utm_campaign=skills-starter). Private AI staff on hardware you own.

A skill is a plain Markdown file of instructions an AI agent follows the same way every time: read the inputs, run the steps, **stop at the approval gate**, hand back the output. No framework, no SDK, no lock-in. If your agent runtime can read Markdown skill files (Claude Code, OpenClaw-style agents, and most Agent Skills-compatible systems), these work.

Watch one run live: [meshvault.ai/skills](https://meshvault.ai/skills?utm_source=github&utm_medium=readme&utm_campaign=skills-starter)

## The skills

| Skill | What it does |
|---|---|
| [`invoice-chaser`](skills/invoice-chaser/SKILL.md) | Finds overdue invoices, drafts friendly nudges in your voice, sends nothing until you approve |
| [`inbox-triage`](skills/inbox-triage/SKILL.md) | Sorts unread email into act, reply, archive, with drafts held for your approval |
| [`daily-standup`](skills/daily-standup/SKILL.md) | Builds a morning brief from your notes, calendar, and tasks. Read only |

## Use them

1. Clone this repo.
2. Drop a skill folder into wherever your agent loads skills (for Claude Code: `~/.claude/skills/`).
3. Ask for the job in plain words: "chase whoever still owes us."

Every skill follows the same shape: **purpose, inputs, steps, approval gate, output.** Open the file, change the rules, keep it. That is the whole point.

## The rule that matters

Nothing leaves the system without a human tapping approve. Every skill here writes that gate into the workflow. Copy that pattern into your own skills before anything else.

## Want more

- **The full pack**: 5 deeper skills, 5 memory templates, 4 operator runbooks, routing recipes and worked examples. [$49 once, no subscription.](https://meshvault.ai/skills?utm_source=github&utm_medium=readme&utm_campaign=skills-starter)
- **The whole system, installed for you**: a private AI operating system on hardware your business owns. [Email us and we set up a live walkthrough.](https://meshvault.ai/contact?utm_source=github&utm_medium=readme&utm_campaign=skills-starter)

## Contribute

Community skills welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). MIT licensed, so build on it.
