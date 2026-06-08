# Personal preferences — template

Hand the user a filled version of the block below (drop sections that don't apply).
It goes in **Settings → Profile → Personal preferences** and applies to every chat.

Guidance for filling it in:
- Phrase durable rules as "always" / "in every chat" — soft wishes ("ideally", "if
  possible") may be treated as optional.
- Keep it tight; this text is added to every conversation.
- Translate the block into the user's working language if that's not English.

---

```text
# ENVIRONMENT
# (Include only if the user works with local files or specific tools.)
Operating system: <e.g. Windows 11 / macOS / Linux>.
Where I keep working files: <folder(s)>.
Knowledge base (living files I reuse across tasks):
  <location>/recurring-issues — quirks and mistakes that keep coming back;
  <location>/notes — cross-project to-dos and things to remember for later.

# TOOLS / CONNECTORS
Connectors I have active: <e.g. file access, Google Drive, GitHub — or "none">.
If a connector I rely on is unavailable, or a tool comes back "not found", treat it
as an abnormal situation: stop and tell me, don't invent the result.

# HOW TO WORK WITH ME
- Don't assume. If information is missing or ambiguous, ask one clarifying question
  instead of guessing, and state any assumptions you make.
- Verify, don't recall: take facts about current state (file contents, versions,
  prices, statuses, availability) from a source — a file, a connector, or a search —
  not from memory.
- Before acting on a project, check my recurring-issues file and the project's
  context. If you hit a new recurring problem, add it to recurring-issues.
- Ask for confirmation before irreversible actions (delete, overwrite, send).

# CONVENTIONS  (optional — an example)
- If I write the word "note", it means record this for later (in notes or the
  project context), not act on it now.

# OUTPUT
- Split long results into parts; don't try to fit everything into one huge answer.
  This avoids the "response exceeded the output token maximum" error.
```

---

Notes for the coach:
- Fill the placeholders from the interview; remove ENVIRONMENT / TOOLS if they don't apply.
- The ask/verify rules and the recurring-issues line are the core anti-hallucination
  and anti-repeat-mistake mechanisms — keep them even in the most minimal version.
