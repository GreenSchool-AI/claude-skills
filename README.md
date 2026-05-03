# Claude Skills for AU Professionals

> Free, open-source [Claude Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview)
> built for working professionals in Australia. Drop a `SKILL.md` into Claude, ask the
> question you'd ask a senior colleague, get back the kind of answer that actually moves work forward.
>
> Built by [Green School AI](https://github.com/GreenSchool-AI) — practical AI training for Australian professionals.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills: 4](https://img.shields.io/badge/Skills-4-2EA44F.svg)](#available-skills)
[![Made in Australia](https://img.shields.io/badge/Made_in-Australia%20%F0%9F%87%A6%F0%9F%87%BA-2EA44F.svg)](https://github.com/GreenSchool-AI)

## What are Claude Skills?

A Claude Skill is a single Markdown file (`SKILL.md`) that turns Claude into a focused
expert on a specific task. Install it once, then any time you ask about that topic Claude
loads the file and follows its instructions — you don't need to repeat yourself or
remember any prompt-engineering tricks.

Read more in [Anthropic's official documentation](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview).

## Available skills

| Skill | What it does | For |
|---|---|---|
| 📄 [**AU Resume & ATS Optimiser**](skills/au-resume-ats-optimiser) | Rewrites your resume for the AU market and the ATS systems used by SEEK, Indeed AU, and LinkedIn | Anyone job-hunting in Australia |
| 💬 [**Workplace Comms Polisher**](skills/workplace-comms-polisher) | Turns a rough email or Slack message into three versions — formal, neutral, friendly — with notes on AU workplace culture | Anyone writing at work who isn't a native English speaker |
| 📋 [**Client Discovery Brief Generator**](skills/client-discovery-brief) | Generates 15–20 diagnostic questions, decomposes deliverables, and flags risks before your first call with a new client | Freelancers and consultants working with AU clients |
| 💡 [**Business Idea Validator**](skills/business-idea-validator) | Takes an AI-related business idea and returns ICP, value prop, MVP options, AU pricing strategy, and a first week of action steps | Small business owners considering an AI product |

## Quick start

1. **Pick a skill** from the list above and open its folder.
2. **Download `SKILL.md`** (right-click → Save link as…) or clone the whole repo:

       git clone https://github.com/GreenSchool-AI/claude-skills.git

3. **Install it** in Claude — see [INSTALL.md](INSTALL.md) for instructions per platform.
4. **Use it** by mentioning what you need ("help me with my resume", "polish this email")
   or by asking Claude to use the skill by name.

## Why we made these

We teach Australian professionals how to use AI well — not as a novelty, but as a daily
working tool. Our students kept asking "can I just use Claude or ChatGPT for this?" and
the honest answer was: yes, but only if you prompt them right. These skills package the
prompting we'd normally write ourselves, so you can install once and forget about it.

If you find them useful and want structured training, check out our courses at
[GreenSchool-AI on GitHub](https://github.com/GreenSchool-AI).

## A note on safety

Skills give Claude instructions to follow. Anthropic
[recommends](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview)
using skills only from trusted sources. Every file in this repo is plain Markdown — no
scripts, no network calls, no hidden behaviour. Read before you install if you want to be
sure: it's all human-readable.

## Contributing

Found a bug? Got an example that should work better? Open an
[issue](../../issues) or start a [Discussion](../../discussions). PRs welcome —
see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE). Use them however you want, including commercially. Attribution
appreciated but not required.

---

<sub>Maintained by [Green School AI](https://github.com/GreenSchool-AI) · For questions, open a [GitHub issue](../../issues)</sub>
