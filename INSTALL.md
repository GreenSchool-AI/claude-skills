# Installing the skills

These skills are plain Markdown files (`SKILL.md`) with a small block of YAML at the top
that tells Claude what the skill does. There's no package manager, no script to run, no
build step. Installation = putting the file in the right folder.

Pick the platform you use Claude on.

## Claude.ai (Pro / Team / Max)

Skills on Claude.ai are managed through the web interface.

1. Open [claude.ai](https://claude.ai) and sign in.
2. Go to **Settings → Capabilities → Skills**.
3. Click **Upload skill** and select the `SKILL.md` file you downloaded.
4. The skill is now available across all your conversations on Claude.ai.

The skill triggers automatically when Claude detects you're asking about something the
skill covers. You can also force it: "Use the AU Resume Optimiser skill to review this
CV."

## Claude Code

Claude Code looks for skills in a specific folder under your home directory.

1. Make sure you have the skills folder (it may already exist):

       mkdir -p ~/.claude/skills/au-resume-ats-optimiser

   (Replace the folder name with whichever skill you're installing.)

2. Move `SKILL.md` into that folder:

       mv ~/Downloads/SKILL.md ~/.claude/skills/au-resume-ats-optimiser/

3. Start a new Claude Code session. The skill loads automatically.

To install **all** the skills in one go, clone the whole repo and symlink:

    git clone https://github.com/GreenSchool-AI/claude-skills.git ~/projects/greenschool-skills
    ln -s ~/projects/greenschool-skills/skills/au-resume-ats-optimiser ~/.claude/skills/au-resume-ats-optimiser
    ln -s ~/projects/greenschool-skills/skills/workplace-comms-polisher ~/.claude/skills/workplace-comms-polisher
    ln -s ~/projects/greenschool-skills/skills/client-discovery-brief ~/.claude/skills/client-discovery-brief
    ln -s ~/projects/greenschool-skills/skills/business-idea-validator ~/.claude/skills/business-idea-validator

Symlinks let you `git pull` updates without re-installing.

## Claude Desktop (macOS / Windows)

1. Open Claude Desktop.
2. Settings → **Capabilities** → **Skills** → **Open skills folder** — this opens the
   folder in Finder/Explorer.
3. Inside that folder, create a subfolder named after the skill, e.g.
   `au-resume-ats-optimiser/`.
4. Drop the `SKILL.md` file inside that subfolder.
5. Restart Claude Desktop.

## Claude API

Skills can be uploaded to the Claude API and used in your own integrations.
See Anthropic's [Skills API Quickstart](https://docs.claude.com/en/docs/agents-and-tools/agent-skills)
for the upload process.

## Verify it works

Start a new chat and ask:

> Which skills do you have available?

The skill you installed should appear in Claude's response. If it doesn't:

- File is named exactly `SKILL.md` (uppercase, no `.txt` on the end — Windows sometimes
  hides extensions).
- Folder name matches the `name` field at the top of `SKILL.md`.
- Claude was restarted (Desktop) or you opened a new session (Claude Code, Claude.ai).

## Troubleshooting

> The skill activates but the answer looks wrong or generic.

LLMs are non-deterministic — sometimes the same prompt produces a weaker answer.
Try once more, or be more specific in what you're asking. If the output is consistently
bad, please [open an issue](https://github.com/GreenSchool-AI/claude-skills/issues) with
the input you sent and what came back. We read everything and patch the skill.

> Claude says it doesn't have access to skills.

Make sure you're on a Claude plan that supports skills. On Claude.ai this currently means
Pro, Team, or Max. The free tier doesn't support skill uploads. Claude Code skills work
regardless of your Claude.ai plan — they're tied to your local Claude Code install.

> The skill triggered when I didn't want it to.

Tell Claude explicitly: "Don't use any skills for this." Or rename the skill folder
temporarily to disable it.
