# CLAUDE.md

## Project Purpose

A single-page habit tracker that lets users add daily habits, mark them complete, and persist progress across sessions — all without a server or build step.

## Tech Stack and Constraints

- Vanilla HTML, CSS, and JavaScript only — no frameworks, no libraries
- No build step; the file is served as-is
- Data persisted in `localStorage`
- Deployed via GitHub Pages from the `main` branch

## File Structure

```
index.html   # entire app: markup, <style>, and <script> in one file
README.md
CLAUDE.md
```

## Code Conventions

- Keep all code in `index.html`; do not split into separate `.css` or `.js` files
- Use `const`/`let`, arrow functions, and template literals (modern ES6+)
- Prefer descriptive variable names over comments
- Keep functions small and single-purpose
- Store app state as a plain array of objects in `localStorage` under the key `habits`

## How to Test

Open `index.html` directly in a browser — no server needed:

```
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

Verify: add a habit, reload the page, confirm it persists. Mark it complete, reload, confirm state is preserved.
