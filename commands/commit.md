---
description: Stage and commit with a generated conventional commit message
agent: orchestrator
---

Review the current staged and unstaged changes (`git status` and `git diff`,
staged first). Propose a conventional commit message (type(scope): summary,
optional body) that accurately describes the staged diff.

Show the user:
1. The files that will be committed (staged paths).
2. The proposed commit message.

Do NOT commit yet. Wait for explicit confirmation from the user. Only after
the user confirms, stage the intended files if needed and run the commit with
the proposed message. If the user asks for changes to the message, revise and
re-confirm before committing.

Never push. Never amend or force-push. If there is nothing staged and nothing
unstaged, say so and stop.
