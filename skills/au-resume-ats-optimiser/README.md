# AU Resume & ATS Optimiser

> A Claude Skill that rewrites your resume for the Australian job market and the ATS
> systems used by SEEK, Indeed AU, and LinkedIn AU.

## What you get

When this skill is active, paste your resume (or attach the file) and Claude will:

- Rewrite weak bullet points using action verbs and metrics, in STAR format.
- Add ATS-friendly keywords for your target role and the AU job sites.
- Format for AU expectations: no photo, no date of birth, no marital status, no headshot,
  page count and section order that matches what AU recruiters actually scan.
- Draft a cover letter tailored to a specific AU job ad if you paste the ad alongside
  your resume.
- Surface the top 3 weak points in your resume with concrete suggestions.
- Run an AU-specific check: formatting that works for SEEK, Indeed AU, and LinkedIn —
  and flag anything that won't.

## Example

See [`examples/`](examples) for a sample marketing manager resume run through the full
optimisation, before and after.

## Install

See the [main INSTALL.md](../../INSTALL.md). The short version:

- **Claude.ai (Pro):** Settings → Capabilities → Skills → Upload `SKILL.md`.
- **Claude Code:** drop `SKILL.md` into `~/.claude/skills/au-resume-ats-optimiser/`.
- **Claude Desktop:** Settings → Skills → Open skills folder → drop file in.

## Use

Once installed, just say what you need:

> Review my resume for an AU marketing role: [paste]

> Here's the job ad and here's my CV — what should I fix?

Or invoke the skill explicitly:

> Use the resume optimiser skill on this: [paste]

## What it's NOT

- It won't replace a recruiter who knows your specific industry. AHPRA, CPA, engineering
  registration — the skill flags these but a real specialist will know more.
- It assumes you already have work rights in Australia. It doesn't cover visa strategy
  or whether your overseas qualifications will be recognised.
- Output quality depends on input quality. A vague three-line resume produces vague
  feedback — give Claude as much context as you can.
- It optimises for AU specifically. If you want to apply in the US or UK, this isn't the
  right skill.

## License

MIT. See [LICENSE](../../LICENSE) in the repo root.

---

<sub>Part of [GreenSchool-AI/claude-skills](../..) ·
Maintained by [Green School AI](https://github.com/GreenSchool-AI) ·
Looking for structured AI training for your job search?
Check out our [Job Search Pack](https://github.com/GreenSchool-AI).</sub>
