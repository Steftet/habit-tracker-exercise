Review the current `index.html` for issues across four categories. Read the file first, then report every finding as a checklist. Do not make any changes.

## Categories

**Bugs** — logic errors or behaviour that diverges from the stated spec (add/delete habits, daily check-off, streak counter, localStorage persistence).

**Missing edge cases** — inputs or states the code does not handle, e.g. empty habit names, duplicate names, very long names, localStorage quota exceeded, habits deleted while completions still reference their id.

**Accessibility** — missing ARIA labels or roles, keyboard-navigation gaps, insufficient colour contrast, focus management after add/delete.

**localStorage errors** — missing try/catch around `JSON.parse` / `JSON.stringify`, no handling of `localStorage` being unavailable (private-browsing quota, `SecurityError`), stale completion keys never pruned.

## Output format

Return a single checklist grouped by category. Mark each finding with its severity:

- `[bug]` — incorrect behaviour
- `[edge]` — unhandled edge case
- `[a11y]` — accessibility issue
- `[storage]` — localStorage reliability issue

Example:

```
### Bugs
- [ ] [bug] …

### Edge cases
- [ ] [edge] …

### Accessibility
- [ ] [a11y] …

### localStorage
- [ ] [storage] …
```

If a category has no findings, write "None found." Do not fix anything — findings only.
