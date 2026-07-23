# opencode-config

My personal [opencode](https://opencode.ai) configuration.

## What's here

- `opencode.json` — main config: plugins, default agent, disabled agents, LSP/formatter settings.
- `tui.json` — TUI theme (`catppuccin`).
- `agents/` — custom agent definitions:
  - `orchestrator.md` — primary agent that routes work between subagents.
  - `architect.md` — produces specs/plans, no file edits.
  - `coder.md` — implements specs with minimal diffs, never commits.
  - `review.md` — reviews uncommitted changes.
  - `escalate.md` — frontier-tier problem solver for stuck tasks.
- `commands/` — custom slash commands:
  - `/review` — run code review on uncommitted changes.
  - `/escalate` — hand a stuck problem to the escalate agent.

## Usage

Clone into `~/.config/opencode/` (or your platform's opencode config dir):

```sh
git clone https://github.com/AlienAscension/opencode-config.git ~/.config/opencode
```

The `superpowers` plugin is pulled automatically from
[github.com/obra/superpowers](https://github.com/obra/superpowers) via the
`plugin` field in `opencode.json`.
