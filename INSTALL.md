# Install

## Claude Code (fastest)

```bash
git clone https://github.com/thefiredev-cloud/meshvault-skills-starter.git /tmp/mv-skills
cp -R /tmp/mv-skills/skills/* ~/.claude/skills/
```

Restart or start a new session. Ask in plain words:

- "Chase overdue invoices"
- "Triage my inbox"
- "Daily standup brief"
- "Draft follow-ups for quiet clients"
- "Prep me for the 2pm call"

## Project-scoped install

```bash
mkdir -p .claude/skills
cp -R /path/to/meshvault-skills-starter/skills/* .claude/skills/
```

## Codex / shared agents root

```bash
cp -R skills/* ~/.agents/skills/
```

## OpenClaw-style or custom loaders

Point the loader at each `skills/<name>/SKILL.md`. Frontmatter uses `name` + `description` so routers can match natural language.

## Verify

Open any `SKILL.md`. Confirm you see **Approval Gate**. If a skill can send, publish, pay, delete, or change accounts, the gate must stop before the action.

## Next

Free samples stop at these five skills. Full operator kit (memory templates, runbooks, routing, worked examples): **$49 once** → https://meshvault.ai/skills
