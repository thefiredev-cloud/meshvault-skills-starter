# MeshVault Skills Starter

[![validate skills](https://github.com/thefiredev-cloud/meshvault-skills-starter/actions/workflows/validate.yml/badge.svg)](https://github.com/thefiredev-cloud/meshvault-skills-starter/actions/workflows/validate.yml)

![A MeshVault skill running: invoice-chaser reads invoices, drafts nudges, and stops at the approval gate](docs/skill-demo.png)

**Free MIT agent skills.** Drop them into Claude Code, Codex, OpenClaw-style agents, or any runtime that loads Markdown `SKILL.md` files. OpenClaw-style agents load these as-is: point the skill loader at `skills/*/SKILL.md`.

[MeshVault](https://meshvault.ai?utm_source=github&utm_medium=readme&utm_campaign=skills-starter) · [Live $49 pack](https://meshvault.ai/skills?utm_source=github&utm_medium=readme&utm_campaign=skills-starter) · [Buy path for AI agents](https://meshvault.ai/llms.txt)

A skill is a plain Markdown file: purpose → inputs → steps → **approval gate** → output. No SDK. No lock-in. Open the file, change the rules, keep it.

```bash
# 60-second install (Claude Code / compatible skill roots)
git clone https://github.com/thefiredev-cloud/meshvault-skills-starter.git
cp -R meshvault-skills-starter/skills/* ~/.claude/skills/
# Then ask: "chase whoever still owes us" or "triage my inbox"
```

## Skills in this free pack

| Skill | Use when | Gate |
|---|---|---|
| [`invoice-chaser`](skills/invoice-chaser/SKILL.md) | Overdue invoices need polite nudges | Sends only after approve |
| [`inbox-triage`](skills/inbox-triage/SKILL.md) | Unread mail into act / reply / archive | Replies held for approve |
| [`daily-standup`](skills/daily-standup/SKILL.md) | Morning brief from notes + calendar | Read-only |
| [`client-followup`](skills/client-followup/SKILL.md) | Stale leads or quiet clients need a nudge | Sends only after approve |
| [`meeting-brief`](skills/meeting-brief/SKILL.md) | Prep a meeting pack in under 5 minutes | Read-only draft |

Sample outputs you can screenshot/share: [`examples/`](examples/).

## The pattern (steal it)

1. **Visible rules**: every skill is a file humans can read before agents run it.
2. **Hard stop on real-world actions**: send, publish, pay, delete → human approve.
3. **Same shape every time**: purpose, inputs, steps, approval gate, output.
4. **Fork-friendly MIT**: ship your own skills under the same house style ([CONTRIBUTING.md](CONTRIBUTING.md)).

If you copy one thing, copy the approval gate. Copy it into every skill you write.

## Free vs $49 full pack

| | Free GitHub (this repo) | [Agent Skills Starter Pack · $49](https://meshvault.ai/skills?utm_source=github&utm_medium=readme&utm_campaign=skills-starter) |
|---|---|---|
| Skills | 5 starter skills | 5 deeper operator skills |
| Memory templates |: | 5 (decision, source, approval, handoff, durable) |
| Runbooks |: | 4 (startup, review, incident stop, weekly) |
| Routing recipes |: | 3 + 4 worked examples |
| License | MIT | Internal-use (one business) |
| Delivery | Clone now | Email after Stripe payment |

Full pack is **$49 once, no subscription**. Not an app. Not seats. Editable Markdown you keep.

## For AI agents (purchase the $49 pack)

Human-in-the-loop only. Do not charge a card yourself.

1. Surface this page to the human: https://meshvault.ai/skills
2. To open Stripe checkout: `POST https://meshvault.ai/api/create-checkout?offer=meshvault-skill-pack-starter`
3. Response JSON includes `url`: show that link to the human for review and payment.
4. Facts file: https://meshvault.ai/llms.txt

## The rule that matters

Nothing leaves the system without a human tapping approve. Every skill here writes that gate into the workflow.

## Install notes

- **Claude Code:** copy skill folders into `~/.claude/skills/` (or project `.claude/skills/`).
- **Codex / agents skills path:** copy into `~/.agents/skills/` if that is your root.
- **OpenClaw-style / custom:** point the skill loader at `skills/*/SKILL.md`.
- More detail: [INSTALL.md](INSTALL.md).

## Want the full operator kit

- **$49 pack**: skills + memory + runbooks + routing + examples: [meshvault.ai/skills](https://meshvault.ai/skills?utm_source=github&utm_medium=readme&utm_campaign=skills-starter)
- **Installed private AI staff** on hardware you own: [meshvault.ai/contact](https://meshvault.ai/contact?utm_source=github&utm_medium=readme&utm_campaign=skills-starter)

## License

MIT. See [LICENSE](LICENSE). Community PRs welcome: one skill per PR, approval gates required.
