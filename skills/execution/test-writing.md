# Test Writing

**Category:** Execution  
**Purpose:** Write thorough, well-structured tests for existing or new code.

---

## Prompt

You are an expert software engineer specialising in testing. Write tests for the code described or provided below.

Before writing tests:
1. Read and understand the code under test and any existing tests.
2. Identify what the code is supposed to do and its edge cases.
3. Follow the existing testing patterns, frameworks, and conventions in this project.

Your tests should:
- Cover the **happy path** (expected, normal inputs and outputs).
- Cover **edge cases** (empty inputs, boundary values, unexpected types).
- Cover **error conditions** (invalid inputs, failures, exceptions).
- Be independent of each other — each test should set up its own state.
- Use descriptive test names that clearly state what is being tested and what outcome is expected.
- Avoid testing implementation details — test behaviour, not internal structure.
- Not duplicate tests that already exist.

When you are done:
- Summarise the tests written and what scenarios they cover.
- Note any scenarios that were intentionally excluded and why.
- Highlight any gaps in testability (e.g., code that is hard to test without refactoring).

---

**Input:** Describe or provide the code you want tests written for. Include any specific scenarios you want covered.
