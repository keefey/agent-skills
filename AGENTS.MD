# Agent Skills

This file defines the universal skills, behaviours, and guidelines that all AI coding agents should follow when working in this repository. Tool-specific configuration files (e.g. `CLAUDE.md`, `.clinerules`, `.roorules`) extend these instructions for their respective environments.

---

## General Principles

- **Minimal changes** – make the smallest possible modification that fully addresses the requirement. Avoid refactoring unrelated code.
- **Read before writing** – always explore and understand existing code before making changes.
- **Explain decisions** – when the approach is non-obvious, leave a concise inline comment or include a note in your response.
- **No secrets in source** – never commit credentials, API keys, tokens, or other sensitive data.
- **Prefer existing libraries** – use what is already in the project; only add new dependencies when strictly necessary.

---

## Coding Standards

- Follow the existing style and conventions of each file you edit (indentation, naming, quote style, etc.).
- Do not add comments unless they match the style of existing comments or are required to explain complex logic.
- Keep functions small and focused on a single responsibility.
- Write self-documenting names for variables, functions, and classes.

---

## Testing

- Run existing tests before and after making changes to confirm nothing is broken.
- Add tests for new behaviour in the same style as existing tests in the project.
- Do not delete or disable existing tests.

---

## Git Hygiene

- Write clear, concise commit messages in the imperative mood (e.g. *"Add retry logic to API client"*).
- Keep each commit focused on a single logical change.
- Never force-push to a shared or protected branch.

---

## Security

- Validate and sanitise all external input.
- Prefer well-known, actively maintained libraries for security-sensitive operations (auth, crypto, etc.).
- Flag potential vulnerabilities in your response even if they are outside the scope of the immediate change.

---

## Communication

- If a requirement is ambiguous, state your interpretation clearly before proceeding.
- If a task cannot be completed safely or correctly, stop and explain why rather than producing a broken or insecure result.

---

## Personas

The skills above are universal. For domain-specific guidance, load the relevant persona file from the [`personas/`](./personas/) directory alongside this file:

| Persona | File | Use when… |
|---------|------|-----------|
| Technical | [`personas/technical.md`](./personas/technical.md) | Writing, reviewing, or debugging code |
| Legal | [`personas/legal.md`](./personas/legal.md) | Researching law, drafting contracts, or assessing compliance |
| Ethics | [`personas/ethics.md`](./personas/ethics.md) | Reviewing decisions, policies, or AI systems for ethical risks |
| Interviews | [`personas/interviews.md`](./personas/interviews.md) | Preparing candidates or designing interview questions |
| General | [`personas/general.md`](./personas/general.md) | Everyday tasks that don't fit a more specialised persona |

To add a new persona, create a file in `personas/` that references this file as its baseline and describes the scope, behaviour, and communication style relevant to that domain.
