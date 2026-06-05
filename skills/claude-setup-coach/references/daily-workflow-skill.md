# Everyday-workflow skill — template

Tailor this to the user's work type, then hand it over as a ready SKILL.md.
It's a normal skill: a folder with this SKILL.md inside. To install: see this repo's
INSTALL.md, or in short — Customize → Skills → "+" → Create skill → Upload.

Tailoring notes:
- General / writing / data work: the template below is ready as-is.
- Coding: also include the rules marked `[CODER]`.
- Match the trigger words in the description to how the user actually talks.

---

```markdown
---
name: daily-workflow
description: >
  Apply my everyday working routine to any task involving files, projects, or
  notes. Triggers: file operations (create, edit, move, delete), mentions of my
  project folders, starting or continuing a project, version control or backups,
  and words like "note", "delete", "remove", "clean up", "project", "continue".
  Use this even when I don't explicitly ask for it.
---

# Everyday workflow

## Before starting
1. Work out which project or context the task belongs to.
2. Read the knowledge base first: the recurring-issues file and (if present) the
   project's context file — BEFORE doing anything.
3. If this is a NEW project, ask whether to track it with version control and
   whether a private backup is wanted. Record the decision in the project context.

## While working
- Don't assume: on missing info, ask one clarifying question rather than guessing.
- Source of truth is files / connectors / search, not memory.
- Irreversible actions (delete, overwrite, send, push) only after confirmation.
- "Note" means record it for later, not act now.
- Produce long output in parts (to avoid the output-token ceiling).

## After working
- New recurring problem → add it to the recurring-issues file.
- Meaningful change in a project → a line in the change log (date, what, why).
- Unfinished work or later ideas → into notes.
- If the project is under version control: offer to commit (show a short message)
  and commit after confirmation — the user often forgets, so prompt them.
- If backup is enabled: after committing, offer to push to the private remote.
  Check there's nothing sensitive before pushing.

## [CODER] extra rules — include only for software work
- Confirm before installing packages, pushing, or deploying.
- Comments and docs in English; never hard-code secrets or tokens.
- Prefer small, focused changes; explain the plan before large edits.
```

---

Reminder for the coach: present this as a clean, copy-paste SKILL.md, with the
`[CODER]` block kept or removed depending on the user.
