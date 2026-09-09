---
description: Commit staged changes with a generated conventional commit message
agent: build
---

Review the staged changes (`git diff --staged`, plus `git status`). Draft a
conventional commit message (type(scope): summary, imperative, max 72-char
header; body only if non-obvious) that accurately describes the staged diff.

Show the user the files to be committed and the proposed message, then run the
commit — the permission prompt is the confirmation gate. If the user rejects
it, ask whether to revise the message or abort; don't assume which.

If nothing is staged, show `git status` and ask what to stage. Never push,
amend, or force-push.
