# Client Discovery Brief Generator

> A Claude Skill that turns "I have a call with a new client tomorrow" into a structured
> discovery brief — diagnostic questions, deliverables, risks, pricing options, follow-up.

## What you get

When this skill is active, describe the prospective client in plain English (industry,
size, what they think they want) and Claude will return:

- 15–20 diagnostic questions, grouped into four categories: current state, problem,
  desired outcome, constraints.
- A decomposition of the client's stated request into concrete deliverables — what
  actually has to ship.
- Hidden risks of the project: scope-creep flags, technical debt warnings, integration
  gotchas you should ask about before quoting.
- Three pricing structures (hourly, fixed, retainer) with arguments for and against each
  in the AU market.
- A draft follow-up email to send within 24 hours of the discovery call.
- AU-specific notes: GST handling on your invoices, ABN requirements in proposals,
  contract language that holds up under AU law.

## Example

See [`examples/`](examples) for a real e-commerce client brief run through the full
process.

## Install

See the [main INSTALL.md](../../INSTALL.md).

- **Claude.ai (Pro):** Settings → Capabilities → Skills → Upload `SKILL.md`.
- **Claude Code:** drop `SKILL.md` into `~/.claude/skills/client-discovery-brief/`.
- **Claude Desktop:** Settings → Skills → Open skills folder → drop file in.

## Use

Once installed:

> I have a call tomorrow with a Melbourne SaaS founder who wants me to build "an AI
> assistant for their support team". Help me prepare.

> What should I ask this client before quoting? [paste their email]

> Price this project three ways: [describe the project].

## What it's NOT

- It won't replace your own judgement on whether a client is a good fit — that's still on
  you.
- It assumes you're a sole trader or running a small services business in AU. Other
  structures (Pty Ltd, partnership) have different tax and contract implications it
  doesn't fully cover.
- It's not legal advice. AU contract templates it suggests are a starting point, not a
  signed agreement — get a lawyer for anything serious.

## License

MIT. See [LICENSE](../../LICENSE) in the repo root.

---

<sub>Part of [GreenSchool-AI/claude-skills](../..) ·
Maintained by [Green School AI](https://github.com/GreenSchool-AI) ·
Building AI products for AU clients? Our [AI Builder track](https://github.com/GreenSchool-AI) is
for you.</sub>
