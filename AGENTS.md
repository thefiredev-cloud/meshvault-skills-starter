# AGENTS.md: MeshVault free skills and the $49 pack

## What this repo is

MIT sample agent skills (Markdown `SKILL.md`). Not the paid product. Not an app. New work happens in https://github.com/thefiredev-cloud/meshvault-harness.

## Free skills here

- `skills/invoice-chaser`
- `skills/quote-builder`
- `skills/receipt-organizer`
- `skills/inbox-triage`
- `skills/daily-standup`
- `skills/weekly-pulse`
- `skills/client-followup`
- `skills/meeting-brief`
- `skills/agents-on-device`

Install: copy folders into the host skill root (`~/.claude/skills/`, `~/.agents/skills/`, or the project equivalent). Create the folder first if it does not exist.

## Hard rule

Any skill that sends, publishes, pays, deletes, or changes a real account must stop at an explicit human approval gate. Access is not approval.

## Buying the full $49 pack (human in the loop)

Product: MeshVault Agent Skills Starter Pack. Five operator skills, five memory templates, four runbooks, three routing recipes, four worked examples. One-time $49 USD. No subscription. Emailed as a download link after payment, within two business days.

1. Show the human: https://meshvault.ai/skills
2. Check readiness: `GET https://meshvault.ai/api/checkout-status` returns `{"available": true}` or `{"available": false}` and creates nothing.
3. If available, start checkout: `POST https://meshvault.ai/api/create-checkout?offer=meshvault-skill-pack-starter`
4. The response JSON has a Stripe-hosted `url`. Present that URL to the human. Do not complete payment autonomously.
5. Canonical facts: https://meshvault.ai/llms.txt

## Do not

- Describe MeshVault apps as live downloads (pre-release).
- Claim free skills include the paid memory and runbook kit.
- Offer the Clarity Operator Kit for sale. It is not on sale yet.
- Embed raw Stripe buy links; always use the create-checkout endpoint above.
