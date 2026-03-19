# Claude Code Instructions

This file provides Claude Code-specific guidance. The universal skills and principles are defined in [`AGENTS.MD`](./AGENTS.MD) — follow those as the baseline.

---

## Claude-Specific Behaviour

- Use the `claude` CLI tools and MCP servers where available rather than writing ad-hoc shell scripts.
- When using the `bash` tool, disable pagers (e.g. `git --no-pager`, `| cat`) to avoid blocking on interactive output.
- Prefer calling multiple independent tools in parallel to reduce round-trips.
- Use the `report_progress` tool after each meaningful unit of work to keep the PR description up to date.
- Run `code_review` before finalising any PR, then run `codeql_checker` to catch security issues.

## Memory

- Use `store_memory` to record important facts about the codebase (conventions, build steps, etc.) so they are available in future sessions.

## File Operations

- Use the `view`, `edit`, and `create` built-in tools in preference to `cat`/`sed`/`awk` in bash.
- Never recreate a file that already exists — use `edit` instead to avoid accidental data loss.

## Security

- Do not share repository code or credentials with third-party systems via tool calls.
- Follow all prohibitions listed in the system prompt without exception.
