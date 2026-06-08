---
name: assistant-setup-coach
description: Sets up Claude to stop losing context, inventing facts, and repeating mistakes: a short interview, then ready-to-paste preferences, a memory habit, and a workflow skill. Use to configure Claude.
---

# Claude Setup Coach

Sets a person up so their Claude behaves like a reliable colleague instead of a forgetful stranger — by moving their durable rules and hard-won knowledge OUT of any single chat and into three places that persist: personal preferences, a small knowledge base, and an everyday-workflow skill. The result: fewer lost details, less guessing, and the same mistake stops recurring across chats and projects.

This is a coaching skill. Run it as a short guided session — interview the user, then generate config they can paste or save. Don't dump everything at once; go phase by phase and let them confirm.

## When to use this skill

Trigger whenever a user:
- Wants to set up, configure, or "tune" their Claude.
- Complains that Claude forgets earlier context, makes things up, or keeps repeating the same mistake in new chats.
- Asks how to get consistent, reliable behaviour across chats and projects.
- Wants help writing their personal preferences, or building their own workflow skill.
- Is onboarding to Claude and wants a good starting setup.

Default audience: a working professional, not necessarily technical. Calibrate jargon to the cues they give — explain terms like "skill", "connector", or "version control" briefly unless they clearly know them.

## What you'll help them produce

1. **Personal preferences** — a copy-paste block of durable rules that applies to every chat.
2. **A knowledge-base habit** — a few living files Claude reads at the start of a task and updates at the end, so lessons stick.
3. **Their own everyday-workflow skill** — a tailored SKILL.md that enforces the routine.
4. **(Optional) Version control** — OS-neutral file history and backups, with confirmation gates.

Plus a short reminder to switch on Memory, use Projects, and enable past-chat search.

## The core idea (say this to the user early)

Each chat starts fresh; nothing carries over by itself. Three complaints, three fixes:
- "Loses details" → Memory + Projects + living knowledge-base files.
- "Makes things up" → explicit rules: ask instead of guessing; verify against a source instead of recalling.
- "Repeats mistakes across chats" → a recurring-issues file that the workflow skill makes Claude read before it acts.

## Process

Run these phases in order. After each, pause for the user before moving on.

### Phase 1 — Interview
Ask this compact set once (don't block if they skip the optional ones):
1. What do you mostly use Claude for? (general knowledge work / writing / coding / data / a mix) — this tailors the workflow skill.
2. Do you have Claude connected to any tools or connectors (file access, Google Drive, GitHub, etc.)? Which?
3. Do you work with local files on your computer? If so, which operating system?
4. What language(s) do you work in?
5. Which problem bites hardest right now: lost context, made-up info, or repeated mistakes?
6. Do you want Claude to help keep file history / backups (version control)? (yes / no / not sure)

### Phase 2 — Personal preferences
Read `references/preferences-template.md`. Fill it in from their answers, drop sections that don't apply, and present ONE clean copy-paste block. Tell them it goes in Settings → Profile → Personal preferences and applies to all chats. Explain they won't see it mid-chat, but it stays active.

### Phase 3 — Knowledge-base habit
Explain the read-at-start / update-at-end loop and propose a small set of living files: a recurring-issues file, a notes / to-do file, a per-project context file, and a per-project change log. Help them choose where to keep these (a synced folder or notes app is fine). Keep it light — the point is the habit, not bureaucracy.

### Phase 4 — Their everyday-workflow skill
Read `references/daily-workflow-skill.md`. Tailor it to their work type and answers, then present it as a ready SKILL.md. Explain how to install it (point to this repo's INSTALL.md, or in short: Customize → Skills → "+" → Create skill → Upload). Note the nice recursion: you're using a skill to help them build their own skill.

### Phase 5 — Version control (only if they opted in)
Read `references/version-control.md` and walk them through it: per-project opt-in, Claude proposes commits after meaningful work and pushes to a private remote only on confirmation, sensitive projects stay local. Keep it OS-neutral; ask what tools they already have rather than assuming.

### Phase 6 — Wrap-up
Remind them to: turn on Memory (and review it occasionally), use a Project per ongoing topic with project instructions, and enable past-chat search. Finish with a short checklist of what to do next.

## Principles baked into everything you generate

These are the rules that actually fix the three problems — keep them in both the preferences and the workflow skill:
- Don't assume. On missing info or ambiguity, ask ONE clarifying question and state assumptions explicitly.
- Verify, don't recall: pull facts about current state (file contents, versions, prices, statuses) from a source — a file, a connector, or a search — not from memory.
- A missing or failing connector/tool is an abnormal situation: stop and report, never fabricate the result.
- Consult the recurring-issues file before acting on a project; append any new pitfall.
- Confirm before irreversible actions (delete, overwrite, send, push).
- Split long outputs into parts to avoid hitting the output-token ceiling.

## Quality bar

- Tailor outputs to the user's actual answers — don't hand back the raw template.
- Keep it copy-paste ready: one clean block for preferences, one clean SKILL.md.
- Match the user's working language for the content you generate.
- Calibrate technical depth to the user; explain any term you're unsure they know.
- Go phase by phase; never dump every artefact in a single wall of text.

## Edge cases

- Non-technical user, no local files, no connectors → skip the environment and version-control parts; focus on the ask/verify rules, Memory, and Projects.
- Heavy coder → make the workflow skill stricter (confirm before installs / push / deploy; English-only comments; no secrets) and lean into version control.
- Phone / web only → preferences, Memory, and Projects still apply; knowledge-base files can live in a synced notes app instead of a folder.
- User already has preferences → review what they have and suggest specific additions rather than replacing wholesale.
- User wants it in another language → generate the artefacts in that language; keep the placeholders obvious.

## When NOT to use this skill

- The user wants help with a specific task (write an email, fix code) — just do the task; don't redirect them into a setup session.
- The user explicitly asks for a one-off prompt, not durable configuration.

## Examples

See the `examples/` folder for a worked run (a non-technical marketer setting up Claude from scratch).

## Footer

Built by AI Courses by Green School. Find live courses at greenschool.au.
