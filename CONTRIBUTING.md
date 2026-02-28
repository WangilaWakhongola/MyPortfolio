# Contributing to MyPortfolio

Thank you for your interest in contributing! This document explains how to get the code running locally, what kinds of contributions are welcome, and the workflow for submitting changes.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Project Structure](#project-structure)
3. [Running Locally](#running-locally)
4. [Making Changes](#making-changes)
5. [Submitting a Pull Request](#submitting-a-pull-request)
6. [Code Style Guidelines](#code-style-guidelines)
7. [Reporting Bugs](#reporting-bugs)
8. [Requesting Features](#requesting-features)

---

## Getting Started

1. **Fork** this repository by clicking the *Fork* button at the top of the page.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<your-username>/MyPortfolio.git
   cd MyPortfolio
   ```
3. Create a **feature branch**:
   ```bash
   git checkout -b feat/your-improvement
   ```

---

## Project Structure

```
MyPortfolio/
├── index.html          # Single-page portfolio (HTML + inline CSS + inline JS)
├── Resume.pdf          # Downloadable résumé
├── README.md           # Project overview and quick-start guide
├── CONTRIBUTING.md     # This file
└── .github/
    ├── workflows/
    │   ├── ci.yml      # HTML validation on every PR
    │   └── static.yml  # Automatic deployment to GitHub Pages
    └── ISSUE_TEMPLATE/ # Bug-report & feature-request templates
```

The entire site lives in **`index.html`** — HTML structure, CSS styles, and JavaScript are all inline in that one file, so there is no build step.

---

## Running Locally

Because the site is a single static HTML file, no package installation is required:

```bash
# Option 1 — open directly in your browser
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Option 2 — serve with Python (avoids some font CORS quirks)
python3 -m http.server 8080
# then visit http://localhost:8080
```

---

## Making Changes

- **HTML/CSS/JS** — edit `index.html` directly.
- Keep changes **focused**: one logical improvement per PR makes review faster and easier.
- After editing, reload the page in your browser and verify the site still looks and works correctly across multiple viewport sizes (mobile, tablet, desktop).

### CI check

Every pull request automatically runs `htmlhint` against `index.html`. You can run the same check locally before pushing:

```bash
npm install --global htmlhint@1
htmlhint index.html
```

Fix any reported issues before opening your PR.

---

## Submitting a Pull Request

1. Push your branch to your fork:
   ```bash
   git push origin feat/your-improvement
   ```
2. Open a **Pull Request** against the `main` branch of this repository.
3. Fill in the pull-request template — describe **what** changed and **why**.
4. Wait for the CI check to go green. If it fails, fix the issues and push again.
5. A maintainer will review your PR and may request changes or merge it.

---

## Code Style Guidelines

- **Indentation**: 2 spaces (no tabs).
- **HTML**: use semantic elements (`<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, etc.).
- **Accessibility**: every `<img>` must have a descriptive `alt` attribute; interactive elements must be keyboard-focusable.
- **CSS**: keep new rules near existing rules of the same component.
- **JavaScript**: use `const`/`let` (never `var`); prefer clear, descriptive variable names.
- **Comments**: add a comment only when the intent is not obvious from the code itself.

---

## Reporting Bugs

Open a **Bug Report** issue using the template provided. Please include:
- Steps to reproduce the problem.
- What you expected to happen.
- What actually happened (screenshots are very helpful).
- Browser name and version.

---

## Requesting Features

Open a **Feature Request** issue using the template provided. Please describe:
- The problem or limitation you are trying to solve.
- Your proposed solution or idea.
- Any alternatives you considered.
