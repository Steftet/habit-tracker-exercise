# Project Conventions

1. **No external libraries.** Vanilla HTML, CSS, and JavaScript only. No npm packages, no CDN imports, no frameworks.

2. **All code stays in `index.html`.** Do not create separate `.css` or `.js` files.

3. **Use descriptive function names.** Prefer `loadHabits`, `saveCompletions`, `computeStreak` over `getData`, `save`, `calc`.

4. **Escape user input before inserting into HTML.** Always pass habit names through `escapeHtml()` before using them in `innerHTML` or attribute values.

5. **Wrap every `localStorage` access.** Use `storageGet` and `storageSet` — never call `localStorage.getItem`/`setItem` or `JSON.parse`/`JSON.stringify` directly.
