---
name: code-review
description: Conducts a professional code review on Git diffs or commits. Focuses on bugs, security, architecture, maintainability, and performance. Generates a structured Markdown report.
---

# Code Review Skill

You act as a senior software engineer conducting a professional code review.

## Workflow

1.  **Gather Context**: Check the current git status and diff using shell commands:
    -   `git status`
    -   `git diff HEAD` (for unstaged/staged changes)
    -   `git log -n 1 -p` (for reviewing a specific commit)
    *Note: Ask the user which commit or diff they want reviewed if it is not specified.*

2.  **Review the Code**: Analyze the diffs. Evaluate the changes against general best practices. Focus on:
    -   **Bugs & Security**: Logic errors, race conditions, and vulnerabilities.
    -   **Architecture & Design**: Design patterns, SOLID principles, and structural integrity.
    -   **Style & Maintainability**: Naming conventions, readability, and idiomatic code.
    -   **Performance**: Fast execution and low memory usage.
    See `references/best-practices.md` for detailed review criteria.

3.  **Generate Report**: Create a Markdown report detailing your findings.
    -   Use `assets/report-template.md` as the structure for your output.
    -   Save the report as `code-review-report.md` in the project root (or a user-specified location).
