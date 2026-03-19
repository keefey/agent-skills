# agent-skills

A collection of reusable AI agent skills and instructions for various coding-assistant tools.

## Structure

### Core files

| File | Purpose |
|------|---------|
| [`AGENTS.MD`](./AGENTS.MD) | Universal skills and principles shared by all agents |
| [`CLAUDE.md`](./CLAUDE.md) | Claude Code-specific extensions |
| [`.clinerules`](./.clinerules) | Cline-specific extensions |
| [`.roorules`](./.roorules) | Roo-specific extensions |

### Personas

Persona files in [`personas/`](./personas/) extend `AGENTS.MD` with domain-specific behaviour. Load the relevant persona alongside the core file for your task.

| Persona | File | Use when… |
|---------|------|-----------|
| Technical | [`personas/technical.md`](./personas/technical.md) | Writing, reviewing, or debugging code |
| Legal | [`personas/legal.md`](./personas/legal.md) | Researching law, drafting contracts, or assessing compliance |
| Ethics | [`personas/ethics.md`](./personas/ethics.md) | Reviewing decisions, policies, or AI systems for ethical risks |
| Interviews | [`personas/interviews.md`](./personas/interviews.md) | Preparing candidates or designing interview questions |
| General | [`personas/general.md`](./personas/general.md) | Everyday tasks that don't fit a more specialised persona |

## How it works

`AGENTS.MD` is the single source of truth for general behaviour (minimal changes, testing, git hygiene, security, etc.). Each tool-specific file references `AGENTS.MD` as the baseline and adds only the configuration or behaviour that is unique to that tool. Persona files layer on top of `AGENTS.MD` with domain-specific scope, behaviour, and communication style.

To add support for a new tool, create a new file following the same pattern and reference `AGENTS.MD` at the top.

To add a new persona, create a new file in `personas/` following the same pattern as the existing persona files.
