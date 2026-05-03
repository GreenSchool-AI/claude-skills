# Workplace Comms Polisher

> A Claude Skill that turns a rough email or Slack message into three versions — formal,
> neutral, friendly — with notes on AU workplace culture and what to use when.

## What you get

When this skill is active, paste your draft email or message and Claude will:

- Rewrite it in three tones: formal (for leadership / clients), neutral (for peers),
  friendly (for your team).
- Explain the difference between the three so you know what to use when.
- Flag anything that clashes with AU workplace culture — directness vs softness, when
  "I'd suggest" beats "I think", how "no worries" actually reads.
- Offer an alternative phrasing if the message is delivering bad news, declining
  something, pushing back, or escalating.
- Suggest three subject lines with different angles.
- Optional "boss-translation": if a message from leadership sounds cryptic, ask the skill
  what it actually means.

## Example

See [`examples/`](examples) for a real "pushing back to my manager" message run through
all three tones.

## Install

See the [main INSTALL.md](../../INSTALL.md).

- **Claude.ai (Pro):** Settings → Capabilities → Skills → Upload `SKILL.md`.
- **Claude Code:** drop `SKILL.md` into `~/.claude/skills/workplace-comms-polisher/`.
- **Claude Desktop:** Settings → Skills → Open skills folder → drop file in.

## Use

Once installed:

> Polish this email to my manager: [paste]

> I need to push back on this without sounding rude: [paste]

> What does this message from my CEO actually mean? [paste]

## What it's NOT

- It won't tell you whether to send a message in the first place — it polishes drafts,
  not strategy.
- It won't fix a fundamentally bad situation. A tone change won't make an unreasonable
  request reasonable.
- AU workplace culture varies — a startup in Melbourne and a bank in Sydney aren't the
  same. The skill assumes a generic AU professional setting; tell Claude if your
  industry is different.

## License

MIT. See [LICENSE](../../LICENSE) in the repo root.

---

<sub>Part of [GreenSchool-AI/claude-skills](../..) ·
Maintained by [Green School AI](https://github.com/GreenSchool-AI) ·
Want to become indispensable at work with AI?
Check out our [AI Power User course](https://github.com/GreenSchool-AI).</sub>
