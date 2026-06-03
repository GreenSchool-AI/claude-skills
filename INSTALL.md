# Installing the skills

Each skill in this repo is a folder containing a `SKILL.md` file (plain Markdown with a
small block of YAML at the top) plus a `README.md` and worked `examples/`. Pick the
platform you use Claude on.

## Claude.ai (web) and Claude Desktop — Windows & macOS

The web app and the desktop app share the same Skills UI, so the steps below apply
identically on Claude.ai in your browser and in Claude Desktop on Windows or macOS.

**Plans:** Skills are available on **Free, Pro, Max, Team, and Enterprise** plans.

**Requirement — turn on code execution:**

- **Free / Pro / Max:** open **Settings → Capabilities** (`claude.ai/settings/capabilities`)
  and enable **Code execution and file creation**.
- **Team:** enabled by default at the organisation level.
- **Enterprise:** an organisation owner enables **Code execution and file creation** and
  **Skills** in **Organization settings → Skills**.

**Install steps:**

**Easiest — use the ready-made ZIP.** Each skill's page in this repo has a one-click
**⬇️ Download the skill (ZIP)** link — for example, the
[AU Resume & ATS Optimiser ZIP](https://github.com/GreenSchool-AI/claude-skills/raw/main/skills/au-resume-ats-optimiser/au-resume-ats-optimiser.zip).
Download that single file, then jump to **"Upload it to Claude"** below. You don't need to
build or zip anything yourself.

**Alternative — build the ZIP yourself** (only if you'd rather inspect or modify the files
first):

1. **Get the skill folder.** Either clone the repo (`git clone https://github.com/GreenSchool-AI/claude-skills.git`)
   or download the whole repo as a ZIP from GitHub (green **Code** button → **Download ZIP**)
   and unzip it.
2. **ZIP the single skill folder.** The ZIP must contain the skill **folder** as its
   root, with `SKILL.md` inside it — not the files loose at the top of the ZIP. The
   folder name must match the skill's `name:` (e.g. `au-resume-ats-optimiser`).

       au-resume-ats-optimiser.zip
       └── au-resume-ats-optimiser/
           ├── SKILL.md
           ├── README.md
           └── examples/

**Upload it to Claude:**

3. In Claude, go to **Customize → Skills** (`claude.ai/customize/skills`).
4. Click the **"+"** button, then **"+ Create skill"**.
5. Select **"Upload a skill."**
6. Upload your ZIP (the one you downloaded, or the one you built).
7. The skill appears in your Skills list. Use the toggle next to it to enable.

**That's it.** The skill triggers automatically when Claude detects you're asking about
something it covers. You can also force it explicitly: "Use the AU Resume & ATS Optimiser
skill to review this CV."

> **Note.** Custom skills you upload are private to your own account. On Team and
> Enterprise plans, an owner can additionally provision skills organisation-wide — see
> Anthropic's help centre for that flow.

## Claude Code

Claude Code reads skills from a folder under your home directory.

1. Create the folder (replace the skill name with whichever you're installing):

       mkdir -p ~/.claude/skills/au-resume-ats-optimiser

2. Copy the skill's files into it (at minimum `SKILL.md`):

       cp -r au-resume-ats-optimiser/* ~/.claude/skills/au-resume-ats-optimiser/

3. Start a new Claude Code session. The skill loads automatically.

To track updates with `git pull`, clone the repo once and symlink the skill instead of
copying:

    git clone https://github.com/GreenSchool-AI/claude-skills.git ~/projects/greenschool-skills
    ln -s ~/projects/greenschool-skills/skills/au-resume-ats-optimiser ~/.claude/skills/au-resume-ats-optimiser

## Claude API

Skills can be uploaded to the Claude API for use in your own integrations. See Anthropic's
[Agent Skills documentation](https://docs.claude.com/en/docs/agents-and-tools/agent-skills)
for the upload process.

## Verify it works

Start a new chat (Claude.ai / Desktop) or a new session (Claude Code) and ask:

> Which skills do you have available?

The skill you installed should appear. If it doesn't, check the troubleshooting list
below.

## Troubleshooting

> **The Skills option doesn't appear in Customize.**

Code execution isn't enabled.
- Free / Pro / Max: **Settings → Capabilities** → enable "Code execution and file
  creation".
- Team / Enterprise: ask an organisation owner to enable code execution and Skills in
  Organization settings.

> **Upload fails with an error.**

Common reasons (per Anthropic's documentation):
- The ZIP exceeds the upload size limit.
- The skill folder name doesn't match the `name:` field in `SKILL.md` frontmatter.
- The required `SKILL.md` is missing, or the files are loose in the ZIP root instead of
  inside the skill folder.
- Invalid characters in the skill name or description.

> **The skill activates but the output looks generic.**

LLMs are non-deterministic — sometimes the same prompt produces a weaker answer. Try
again, or be more specific. If it's consistently off, please
[open an issue](https://github.com/GreenSchool-AI/claude-skills/issues) with the input you
sent and what came back — we read everything and patch the skill.

> **The skill triggered when I didn't want it to.**

In **Customize → Skills**, toggle the skill off, or tell Claude explicitly: "Don't use any
skills for this." Re-enable when you need it.

> **Skills look greyed out.**

Code execution is disabled — at the organisation level (Team / Enterprise) or individually.
Enable it in **Settings → Capabilities** (Free / Pro / Max) or check with your
organisation owner (Team / Enterprise).
