# CLAUDE.md — AI Assistant & Project Guidelines

This file provides context for AI assistants (e.g., Claude in Cursor) working on the FlyRank capstone repository.

## Project Overview

FlyRank is a Node.js capstone project. Follow existing patterns in the codebase before introducing new abstractions or dependencies.

## Coding Conventions

### General

- Use **Node.js LTS** features and syntax.
- Prefer **clear, readable code** over clever one-liners.
- Keep changes **focused and minimal** — solve the task at hand without unrelated refactors.
- Match the **style and structure** of surrounding files (naming, imports, formatting).

### JavaScript / Node.js

- Use `const` by default; use `let` only when reassignment is required.
- Prefer `async/await` over raw Promise chains for asynchronous code.
- Handle errors explicitly; avoid silent failures.
- Use meaningful variable and function names (camelCase for variables/functions, PascalCase for classes).
- Add comments only for non-obvious logic — code should be self-explanatory where possible.

### File Organization

- Place source code under a dedicated directory (e.g., `src/`) once the project structure is established.
- Keep configuration at the project root (`package.json`, `.env.example`, etc.).
- Do not commit secrets, credentials, or local environment files.

## Git Workflow

### Branches

- `main` — stable, deployable code.
- Feature branches: `feature/<short-description>` (e.g., `feature/user-ranking`).
- Bug fixes: `fix/<short-description>`.

### Commits

- Write **clear, imperative commit messages** (e.g., "Add ranking score calculator", not "Added stuff").
- Keep commits **atomic** — one logical change per commit.
- Do not commit `.env`, `node_modules/`, or other ignored files.

### Pull Requests

- Open a PR from a feature branch into `main`.
- Include a brief summary of changes and how to test them.
- Resolve review feedback before merging.

## AI Assistant Guidelines

When assisting on this project:

1. **Read before writing** — inspect relevant files and conventions before making changes.
2. **Minimize scope** — implement only what was requested; avoid drive-by refactors.
3. **Do not commit unless asked** — stage and commit only when the user explicitly requests it.
4. **Do not push unless asked** — never force-push to `main`.
5. **Preserve secrets** — never add API keys, tokens, or passwords to tracked files.
6. **Explain trade-offs** — when multiple approaches exist, briefly state the chosen approach and why.
7. **Verify changes** — run tests or lint commands when available; report if they cannot be run.
8. **Use existing tools** — prefer project scripts (`npm test`, `npm run lint`) over ad-hoc commands when defined.

## Stack Reference

| Tool       | Purpose                          |
| ---------- | -------------------------------- |
| Node.js    | Runtime and application logic    |
| Git        | Local version control            |
| GitHub     | Remote repository and collaboration |
| Cursor IDE | Development environment and AI-assisted coding |

## Getting Started (for assistants)

When the user asks to set up or extend the project:

1. Check for `package.json` and install dependencies with `npm install` if present.
2. Look for `.env.example` and remind the user to copy it to `.env` if environment variables are required.
3. Follow patterns established in `README.md` and this file.
