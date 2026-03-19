# Contributing a New Skill

Anyone can add a new skill to this repository. Follow the steps below to contribute.

## What is a skill?

A skill is a reusable prompt designed to give an AI agent a specific capability or role. Skills are grouped into two categories:

| Category | Description |
|----------|-------------|
| **[Advice & Guidance](skills/advice-guidance/)** | The agent reviews, evaluates, or recommends — but does not make changes. |
| **[Execution](skills/execution/)** | The agent actively performs a task and produces a concrete output. |

## How to add a new skill

### 1. Choose a category

Decide whether your skill is **Advice & Guidance** or **Execution** (see descriptions above).

### 2. Create a skill file

Create a new Markdown file in the appropriate directory:

```
skills/advice-guidance/<your-skill-name>.md
skills/execution/<your-skill-name>.md
```

Use lowercase words separated by hyphens for the filename (e.g., `dependency-audit.md`).

### 3. Use the skill template

Copy the template below into your new file and fill in each section:

```markdown
# <Skill Name>

**Category:** <Advice & Guidance | Execution>  
**Purpose:** <One sentence describing what this skill does.>

---

## Prompt

<The full prompt text the agent will use. Be specific about the agent's role, what it should do, and how it should format its output.>

---

**Input:** <Describe what the user should provide when using this skill.>
```

### 4. Register your skill in the category README

Open the `README.md` in the relevant category directory and add a row to the skills table:

```markdown
| [your-skill-name.md](your-skill-name.md) | Short description of the skill |
```

### 5. Open a pull request

Submit a pull request with:

- Your new skill file
- The updated category `README.md`

Include a brief description in your PR explaining what the skill does and when someone would use it.

## Guidelines

- **One skill per file.** Keep each file focused on a single, well-defined capability.
- **Be specific.** Vague prompts produce vague results. Define the agent's role, expected output format, and any constraints clearly.
- **Test your skill.** Try the prompt with an AI agent before submitting to make sure it works as intended.
- **Use plain Markdown.** No special tooling required — just text.
