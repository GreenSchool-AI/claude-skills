# Business Idea Validator

> A Claude Skill that takes an AI-related business idea and returns a complete first
> validation pass — the kind of work a $300/hour business coach would do — in two minutes.

## What you get

Describe your idea in 2–20 sentences ("AI beauty advisor for my salon clients", "AI
scheduling helper for my landscaping business") and Claude will return:

- **ICP** — Ideal Customer Profile. Who specifically buys this. Where to find the first
  ten of them.
- **Value proposition** in Steve Blank format: "We help [target] who [problem] by
  [solution] unlike [alternative]."
- **Three MVP options** at different cost and time investments — from "test the idea
  this weekend" to "spend 6 weeks building it properly".
- **Pricing strategy in AUD** — from "cheap entry" to "premium positioning", with
  reasoning for the AU market.
- **Top 5 risks** with concrete mitigations.
- **First three steps for this week** — specific, actionable, no fluff.
- **AU-specific notes:** GST on your pricing, BAS implications, Fair Trading rules for
  outreach to potential customers.

## Example

See [`examples/`](examples) for a "AI beauty advisor for an existing salon" idea run
through the full validation.

## Install

See the [main INSTALL.md](../../INSTALL.md).

- **Claude.ai (Pro):** Settings → Capabilities → Skills → Upload `SKILL.md`.
- **Claude Code:** drop `SKILL.md` into `~/.claude/skills/business-idea-validator/`.
- **Claude Desktop:** Settings → Skills → Open skills folder → drop file in.

## Use

Once installed:

> I'm a personal trainer in Brisbane. What if I built an AI that creates personalised
> nutrition plans for my clients? Validate this idea for me.

> Could I sell an AI scheduling assistant to other tradies?

> Help me figure out if this is worth doing: [paste your idea]

## What it's NOT

- It's not a substitute for actually talking to ten potential customers. The skill gives
  you a structured first pass — you still need to validate with real humans.
- It's not legal or financial advice. The AU-specific notes are starting points, not
  compliance.
- It can't tell you if your idea will succeed. Nobody can. It can tell you whether it's
  worth investing the next 4 weeks finding out.
- It assumes you're staying small (sole trader, small Pty Ltd). Venture-scale strategy is
  different and not covered.

## License

MIT. See [LICENSE](../../LICENSE) in the repo root.

---

<sub>Part of [GreenSchool-AI/claude-skills](../..) ·
Maintained by [Green School AI](https://github.com/GreenSchool-AI) ·
Ready to actually build the thing? Our [AI Founder Pack](https://github.com/GreenSchool-AI) takes
you from idea to first paying customer.</sub>
