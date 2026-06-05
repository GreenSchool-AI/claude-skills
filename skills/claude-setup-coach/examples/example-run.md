# Example run — a non-technical marketer setting up from scratch

A worked example of the Claude Setup Coach in action. Abridged.

## The interview (the user's answers)
1. Mostly: writing — emails, social posts, campaign briefs.
2. Connectors: Google Drive only.
3. Local files: no — everything lives in Google Drive (on a Mac, rarely touches the file system).
4. Language: English.
5. Worst problem: Claude repeats the same mistakes — keeps using a banned phrase and the wrong product name.
6. Version control: not sure → skip for now.

## What the coach produced

### 1. Personal preferences (paste into Settings → Profile)
```text
# TOOLS / CONNECTORS
Connectors I have active: Google Drive. If it's unavailable or a tool comes back
"not found", treat it as abnormal: stop and tell me, don't invent the result.

# HOW TO WORK WITH ME
- Don't assume. On missing info or ambiguity, ask one clarifying question and state
  your assumptions.
- Verify, don't recall: pull facts (names, figures, current details) from the Drive
  document or a search, not from memory.
- Before writing copy, check my "recurring-issues" note for banned phrases and the
  correct product names. If I correct you on something new, add it there.

# OUTPUT
- Split long results into parts to avoid the output-token-limit error.
```

### 2. Knowledge-base habit
One Google Doc named `recurring-issues` with two short lists: "banned phrases" and
"correct names". The workflow skill reads it before drafting and appends new fixes.

### 3. Everyday-workflow skill (installed once)
A trimmed `daily-workflow` SKILL.md (no `[CODER]` rules) whose key line is: "Before
drafting copy, read recurring-issues; after any correction, add the fix to it."

## Result
The repeated-mistake problem is now handled by the recurring-issues loop: once a fix
is written down, it survives into every new chat instead of being re-explained. The
ENVIRONMENT and version-control sections were dropped because they didn't apply —
the coach tailors to the answers rather than handing over the whole template.
