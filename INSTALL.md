# Installing the skills

These skills are plain Markdown files (`SKILL.md`) with a small block of YAML at the top
that tells Claude what the skill does. Pick the platform you use Claude on.

## Claude.ai (web) and Claude Desktop — Windows & macOS

The web app and the desktop app share the same UI for skills, so the steps below apply
identically on Claude.ai in your browser and in Claude Desktop on either Windows or
macOS.

**Requirements:**

- A Claude account on any plan (Free, Pro, Max, Team, Enterprise).
- **Code execution and file creation** enabled.
  - On Free / Pro / Max: open **Settings → Capabilities** and toggle it on.
  - On Team / Enterprise: ask your organization owner to enable it in
    **Organization settings → Skills**.

**Install steps:**

1. **Download `SKILL.md`** for the skill you want from this repo. Open the file on
   GitHub, then click **Download raw file** (top-right of the file viewer).
2. In Claude, open **Customize → Skills**. The Customize panel is reachable from any
   of the three workspaces — Chat, Cowork, or Code — via the sidebar.
3. Click the **"+"** button at the top of the skill list → **Create skill** →
   **Upload skill**.
4. A drag-and-drop modal appears. Either:
   - **Drag `SKILL.md`** onto the drop zone, or
   - **Click the drop zone** to open a file picker and select `SKILL.md`.
5. The skill appears in your Skills list. Use the toggle next to it to enable.

**That's it.** The skill triggers automatically when Claude detects you're asking about
something it covers. You can also force it explicitly: "Use the AU Resume Optimiser
skill to review this CV."

> **A note on file format.** Anthropic's official documentation says to upload a **ZIP
> file containing your skill folder**. For our skills (single `SKILL.md`, no bundled
> scripts or assets) the upload modal accepts the bare `.md` file directly, and that's
> the simplest path. If for any reason the upload fails, fall back to ZIP: put
> `SKILL.md` inside a folder named after the skill (e.g. `au-resume-ats-optimiser/`),
> ZIP that folder, and upload the ZIP instead.

## Claude Code

Claude Code reads skills from a folder under your home directory.

1. Create the folder if it doesn't exist (replace the skill name with whichever you're
   installing):

       mkdir -p ~/.claude/skills/au-resume-ats-optimiser

2. Move `SKILL.md` into that folder:

       mv ~/Downloads/SKILL.md ~/.claude/skills/au-resume-ats-optimiser/

3. Restart Claude Code or start a new session. The skill loads automatically.

To install **all** skills at once, clone the repo and symlink:

    git clone https://github.com/GreenSchool-AI/claude-skills.git ~/projects/greenschool-skills
    ln -s ~/projects/greenschool-skills/skills/au-resume-ats-optimiser ~/.claude/skills/au-resume-ats-optimiser
    ln -s ~/projects/greenschool-skills/skills/workplace-comms-polisher ~/.claude/skills/workplace-comms-polisher
    ln -s ~/projects/greenschool-skills/skills/client-discovery-brief ~/.claude/skills/client-discovery-brief
    ln -s ~/projects/greenschool-skills/skills/business-idea-validator ~/.claude/skills/business-idea-validator

Symlinks let you `git pull` updates without re-installing.

## Claude API

Skills can be uploaded to the Claude API for use in your own integrations. See
Anthropic's [Skills API quickstart](https://docs.claude.com/en/docs/agents-and-tools/agent-skills)
for the upload process.

## Verify it works

Start a new chat (Claude.ai / Desktop) or a new session (Claude Code) and ask:

> Which skills do you have available?

The skill you installed should appear in Claude's response. If it doesn't:

- File is named exactly `SKILL.md` (uppercase, no `.txt` on the end — Windows sometimes
  hides extensions).
- The skill is **toggled ON** in Customize → Skills (in Claude.ai / Desktop).
- For Claude Code: the folder name matches the `name:` field in the frontmatter at the
  top of `SKILL.md`.
- Restart Claude Desktop, or start a fresh session in Claude.ai / Claude Code.

## Troubleshooting

> **The Skills option doesn''t appear in Customize.**

Code execution isn''t enabled on your account.
- Free / Pro / Max: open **Settings → Capabilities** → enable
  "Code execution and file creation".
- Team / Enterprise: ask your organization owner to enable Code execution and Skills
  in Organization settings.

> **Upload fails with an error.**

Common reasons (per Anthropic''s documentation):
- File or ZIP size exceeds the upload limit.
- For ZIP uploads: folder name doesn''t match the `name:` field in `SKILL.md`
  frontmatter.
- File is not `SKILL.md` (case matters; uppercase only).
- Invalid characters in skill name or description.

> **The skill activates but the output looks wrong or generic.**

LLMs are non-deterministic — sometimes the same prompt produces a weaker answer.
Try once more, or be more specific in what you''re asking. If the output is
consistently off, please [open an issue](https://github.com/GreenSchool-AI/claude-skills/issues)
with the input you sent and what came back. We read everything and patch the skill.

> **The skill triggered when I didn''t want it to.**

In Customize → Skills, toggle the skill OFF for that conversation, or tell Claude
explicitly: "Don''t use any skills for this." Re-enable when you need it.

> **I''m on the free plan and Skills look greyed out.**

Code execution must be enabled in **Settings → Capabilities** on the free plan too.
Skills themselves are available on all plans now (Anthropic enabled this earlier in
2026), but they all require code execution.