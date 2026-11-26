# React / JSX notes

Short JSX-specific rules. Normative HTML rules still apply via [whatwg-elements-index.md](whatwg-elements-index.md).

## Attribute mapping

| HTML | JSX |
|------|-----|
| `class` | `className` |
| `for` | `htmlFor` |
| `tabindex` | `tabIndex` |
| `readonly` | `readOnly` |
| `maxlength` | `maxLength` |
| `colspan` / `rowspan` | `colSpan` / `rowSpan` |
| `datetime` | `dateTime` |
| `autocomplete` | `autoComplete` |
| `crossorigin` | `crossOrigin` |

**Spec (attributes):** [Global attributes](https://html.spec.whatwg.org/multipage/dom.html#global-attributes)

## Document shell

| Rule | Detail |
|------|--------|
| One `main` per page | Place in app shell (`layout.js` / root page), not in every route component |
| Landmarks | `header`/`nav`/`footer` in shell; page content in `main` |
| Fragments | `<>...</>` does not create a landmark — first real child defines semantics |

## Common patterns

```jsx
// Good: semantic button
<button type="button" onClick={handleClick}>Save</button>

// Good: form label association
<label htmlFor="email">Email</label>
<input id="email" type="email" name="email" autoComplete="email" />
```

## `dialog` caveats

| Topic | Note |
|-------|------|
| Hydration | `<dialog open>` vs `showModal()` — prefer client-only open to avoid mismatch |
| Focus | `showModal()` traps focus; ensure close button is in tab order |
| SSR | Render closed; open via `useEffect` after mount |
| Native close | `onClose` + `method="dialog"` on submit buttons |

**Spec:** [#the-dialog-element](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-dialog-element)

## `details` / `summary`

Works in SSR without JS. Don't replace with custom accordion unless behavior requires it.

## Avoid

- `<p className={…}>` wrapping block children (invalid nesting — use `div` or fix structure)
- Self-closing non-void elements (`<div />` with children elsewhere)
- `dangerouslySetInnerHTML` when structured markup would work

## Deeper React a11y

Pair with `web-design-guidelines` skill for component-level accessibility patterns.