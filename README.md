# opencode-config

My personal [opencode](https://opencode.ai) configuration.

## Topology

One primary engineer (`build`, the overridden built-in) does the work directly
— reads, plans, edits, tests, commits. It delegates only:

- `@explore` (built-in, flash model) — noisy read-only research
- `@review` (qwen3.7-max) — fresh-eyes diff review
- `@general` (built-in) — parallel independent work units, user-gated
- `@code-reviewer` (superpowers plugin) — skill-driven reviews

`plan` (built-in) is the read-only analysis mode. The `openwebui` provider
(local Open WebUI models) stays configured for manual model switching via
`/models`.

## Files

- `opencode.json` — models, centralized permissions, agent overrides, MCP, LSP.
- `tui.json` — TUI theme (catppuccin).
- `agents/` — `build.md` (primary), `review.md` (subagent).
- `commands/` — `/commit`, `/review` (both execute through `build`).

## Usage

Clone into `~/.config/opencode/` (or your platform's opencode config dir):

    git clone https://github.com/AlienAscension/opencode-config.git ~/.config/opencode

The `superpowers` plugin is pulled automatically from
github.com/obra/superpowers via the `plugin` field in `opencode.json`.

## Reverting

The old topology (orchestrator/architect/coder/escalate + heretic/canon) was
backed up before the streamlining; restore individual agent files from
`/tmp/opencode/backup/opencode-config/` if ever needed, then restart opencode.
