# agent-skills

A collection of reusable AI agent skills and instructions for various coding-assistant tools.

## Structure

| File | Purpose |
|------|---------|
| [`AGENTS.MD`](./AGENTS.MD) | Universal skills and principles shared by all agents |
| [`CLAUDE.md`](./CLAUDE.md) | Claude Code-specific extensions |
| [`.clinerules`](./.clinerules) | Cline-specific extensions |
| [`.roorules`](./.roorules) | Roo-specific extensions |

## How it works

`AGENTS.MD` is the single source of truth for general coding behaviour (minimal changes, testing, git hygiene, security, etc.). Each tool-specific file references `AGENTS.MD` as the baseline and adds only the configuration or behaviour that is unique to that tool.

To add support for a new tool, create a new file following the same pattern and reference `AGENTS.MD` at the top.
