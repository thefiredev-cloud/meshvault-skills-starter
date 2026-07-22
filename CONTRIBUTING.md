# Contributing

Community skills are welcome. Keep them in the house style:

1. One folder under `skills/`, one `SKILL.md` inside it.
2. Frontmatter: `name`, `description` (write it as "This skill should be used when the user asks..."), `license: MIT`, and a version.
3. Body sections in this order: purpose line, **Required Inputs**, **Steps**, **Approval Gate**, **Output**.
4. Any step that sends, publishes, pays, deletes, or changes account state must stop at the approval gate. Skills that act without a gate will not be merged.
5. Plain language. If a 12 year old cannot follow the steps, simplify them.
6. No credentials, no client data, no personal information in examples.

Open a pull request with the new folder. One skill per PR.
