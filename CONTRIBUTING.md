# Contributing to MindMate

Thank you for your interest in contributing to MindMate! This guide explains how to get started, what we expect from contributors, and how the review process works.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Features](#suggesting-features)
  - [Submitting Pull Requests](#submitting-pull-requests)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Review Process](#review-process)

---

## Code of Conduct

By participating in this project you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

---

## How to Contribute

### Reporting Bugs

1. Search [existing issues](https://github.com/search?q=org%3AMindMate-Project&type=issues) to avoid duplicates.
2. Open a new issue using the **Bug Report** template.
3. Include a clear title, steps to reproduce, expected vs. actual behavior, and relevant environment details.

### Suggesting Features

1. Search existing issues to see whether the idea has been discussed before.
2. Open a new issue using the **Feature Request** template.
3. Describe the problem you are solving, the proposed solution, and any alternatives you considered.

### Submitting Pull Requests

1. **Fork** the relevant repository and create a branch from `main`.
2. Keep changes focused — one feature or fix per PR.
3. Write or update tests to cover your changes.
4. Ensure all tests pass and linting is clean before opening the PR.
5. Fill in the pull request template completely.
6. Link any related issues using keywords such as `Closes #123`.

---

## Development Setup

Refer to each repository's own README for local setup instructions:

- [Backend](https://github.com/MindMate-Project/Backend#-prerequisites--setup-locally)
- [Web App](https://github.com/MindMate-Project/alzaheimer-web#available-scripts)
- [AI Service](https://github.com/MindMate-Project/AI)

---

## Coding Standards

### Backend (TypeScript / Node.js)

- Use TypeScript strict mode.
- Follow the existing project structure — controllers, services, models, routes.
- Validate all user input using existing middleware patterns.
- Add Swagger annotations for any new or modified endpoints.

### Web App (React / JavaScript)

- Use functional components and React hooks.
- Manage global state through Redux Toolkit slices.
- Keep component files small and focused.

### AI Service (Python)

- Follow PEP 8 style conventions.
- Document new functions and classes with docstrings.
- Pin dependency versions in `requirements.txt`.

---

## Commit Message Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

**Examples:**

```
feat(reminders): add SMS notification support
fix(auth): resolve token expiry edge case
docs(api): update Swagger annotations for alerts endpoint
```

---

## Review Process

1. A maintainer will review your PR within a few business days.
2. You may be asked to make changes — please respond promptly.
3. Once approved, a maintainer will merge the PR.
4. All contributions are subject to the repository's license.

---

Thank you for helping make MindMate better for Alzheimer's patients and their caregivers! 🧠❤️
