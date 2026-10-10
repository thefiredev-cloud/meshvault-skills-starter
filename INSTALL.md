# Install

## Claude Code (fastest)

```bash
git clone https://github.com/thefiredev-cloud/meshvault-skills-starter.git /tmp/mv-skills
mkdir -p ~/.claude/skills
cp -R /tmp/mv-skills/skills/* ~/.claude/skills/
```

`cp -R` overwrites skill folders that already have the same name.

Restart or start a new session. Ask in plain words:

- "Chase overdue invoices"
- "Draft a quote from the approved price list"
- "Sort these receipts"
- "Triage my inbox"
- "Daily standup brief"
- "Give me the weekly pulse from these approved files"
- "Draft follow-ups for quiet clients"
- "Prep me for the 2pm call"
- "Put a gated agent on this machine"

## Project-scoped install

```bash
mkdir -p .claude/skills
cp -R /path/to/meshvault-skills-starter/skills/* .claude/skills/
```

## Codex

User-wide skills live in `~/.agents/skills/`. Repo skills live in `.agents/skills/` inside the repo. From the cloned folder:

```bash
mkdir -p ~/.agents/skills
cp -R skills/* ~/.agents/skills/
```

## Other loaders

Point the loader at each `skills/<name>/SKILL.md`. Front matter uses `name` and `description` so routers can match natural language.

## Verify

Open any `SKILL.md` and confirm it has an `## Approval Gate` section. If a skill can send, publish, pay, delete, or change accounts, the gate must stop before the action.

## Next

The free skills are the MIT files in this repo. The paid pack adds memory templates, runbooks, routing recipes, and worked examples for $49 once: https://meshvault.ai/skills
