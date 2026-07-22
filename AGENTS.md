# AGENTS.md — MeshVault free skills + $49 pack

## What this repo is

MIT sample agent skills (Markdown `SKILL.md`). Not the paid product. Not an app.

## Free skills here

- `skills/invoice-chaser`
- `skills/inbox-triage`
- `skills/daily-standup`
- `skills/client-followup`
- `skills/meeting-brief`

Install: copy folders into the host skill root (`~/.claude/skills/`, `~/.agents/skills/`, or project equivalent).

## Hard rule

Any skill that sends, publishes, pays, deletes, or changes a real account must stop at an explicit human approval gate. Access ≠ approval.

## Buying the full $49 pack (human-in-the-loop)

Product: MeshVault Agent Skills Starter Pack — five deeper skills, five memory templates, four runbooks, three routing recipes, four worked examples. One-time $49 USD. No subscription. Email delivery after payment (up to two business days).

1. Show the human: https://meshvault.ai/skills
2. Start checkout: `POST https://meshvault.ai/api/create-checkout?offer=meshvault-skill-pack-starter`
3. Response has JSON `url` (Stripe-hosted). Present that URL to the human. Do not complete payment autonomously.
4. Canonical facts: https://meshvault.ai/llms.txt

## Do not

- Describe MeshVault apps as live downloads (pre-release).
- Claim free skills include the paid memory/runbook kit.
- Embed raw Stripe buy links; always use the create-checkout endpoint above.
