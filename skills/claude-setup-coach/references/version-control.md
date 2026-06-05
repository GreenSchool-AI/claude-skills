# Version control — optional module (OS-neutral)

Use only if the user opted in. The goal: file history and an off-site backup, with
Claude doing the bookkeeping the user tends to forget — but always after confirmation.

## Tool-agnostic — ask first
Don't assume an operating system or installed tools. Ask what they already have:
- A version-control system installed? (git is the common choice.)
- An account with a remote host for backups? (GitHub, GitLab, Bitbucket, etc.)
- A command-line tool for that host? (Optional — it makes sign-in and pushing easier.)

If something's missing, offer to walk them through installing it with whatever
package manager their platform uses — but confirm before installing anything.

## How it works per project (two opt-ins)
1. **Local history.** At the start of a project, ask: "track this with version
   control?" On yes, initialise it and make a first snapshot. After meaningful work,
   propose a commit (show a short message) and commit on confirmation.
2. **Backup to a remote.** A separate opt-in: "back this up to a private remote?"
   On yes, create a PRIVATE repository and push there. Push only after confirmation.

Record both decisions in the project's context file so you don't re-ask each time.

## Privacy (important)
- Remote repositories default to PRIVATE.
- Sensitive projects (personal documents, health data, passwords/tokens) stay under
  local version control only — no remote.
- Before any push, check the snapshot for secrets; use an ignore file for junk and
  temporary files.

## Why Claude drives this
People forget to commit. Letting Claude propose the commit or backup at natural
checkpoints — and execute on a quick "yes" — keeps the history useful without taking
the decision away from the user. Initiative sits with Claude; control stays with the user.
