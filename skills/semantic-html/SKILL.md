---
name: semantic-html
description: WHATWG-conformant semantic HTML procedure for accessibility and SEO. Use when refactoring markup, reviewing HTML/JSX structure, fixing invalid nesting, improving accessibility, or when the user asks for "semantic tags," "semantic HTML," "proper HTML structure," "accessibility markup," or "replace div/span with semantic elements."
metadata:
  version: 2.0.0
---

# Semantic HTML (WHATWG v2)

Apply meaning-first HTML per the [WHATWG Living Standard](https://html.spec.whatwg.org/multipage/). Prefer semantic elements over generic `<div>`/`<span>` when the meaning fits.

## When to Use This Skill

- Refactoring markup (div soup → semantic structure)
- Page layout (header, main, nav, footer, sections)
- **Markup review** / **invalid nesting** fixes
- Accessible markup implementation or review
- Forms, tables, media, interactive UI (`details`/`dialog`)
- React/JSX semantic structure

## Procedure

1. **Landmarks + outline** — One `main`, one `h1`, logical heading order (`h1`→`h2`→…). Map regions to `header`/`nav`/`main`/`aside`/`footer`/`section`/`article`.
2. **Pick element** — Apply [tier-a-daily.md](references/tier-a-daily.md) first; if not listed, search [whatwg-elements-index.md](references/whatwg-elements-index.md).
3. **Validate nesting** — Check parent/child against [content-models.md](references/content-models.md).
4. **Reject obsolete** — Forbidden elements in [obsolete.md](references/obsolete.md); refuse and propose replacements.
5. **React/JSX** — If JSX, read [react-notes.md](references/react-notes.md) (`className`, `htmlFor`, one `main` in app shell).
6. **Cite spec** — When fixing or disputing, include the WHATWG multipage URL from the catalog in review comments.

## Tier A (daily)

Mandatory on every task — full checks in references:

| Region / pattern | Element |
|------------------|---------|
| Page shell | `header`, `nav`, `main`, `aside`, `footer` |
| Content blocks | `section`, `article`, `p`, `ul`/`ol`/`li` |
| Actions | `a` (navigation), `button` (action) — not `div`+click |
| Media | `img` (`alt`), `figure`+`figcaption` |
| Forms | `form`, `label`, `input`, `textarea`, `select` |

## On-demand references

Installed path: `.agents/skills/semantic-html/references/`

| File | When |
|------|------|
| [tier-b-on-demand.md](references/tier-b-on-demand.md) | Forms validation, tables, media, `dialog`/`details` |
| [tier-c-on-demand.md](references/tier-c-on-demand.md) | Rare: `ruby`, `abbr`, `datalist`, `output`, `meter`… |
| [whatwg-elements-index.md](references/whatwg-elements-index.md) | Full element catalog + spec links |
| [content-models.md](references/content-models.md) | Nesting rules |
| [obsolete.md](references/obsolete.md) | Forbidden tags |
| [react-notes.md](references/react-notes.md) | JSX caveats |

## Core rules (summary)

1. **Meaning over layout** — No semantic element fits → `div`/`span` OK.
2. **One `<main>`** per document (hierarchically correct).
3. **No heading skips** — Single `h1`; don't use headings for size.
4. **No obsolete/presentational** — See [obsolete.md](references/obsolete.md).

## Quick refactor

1. Identify blocks → landmarks.
2. Fix heading outline.
3. Replace list/quote/figure/form divs with proper elements.
4. Validate nesting; reject obsolete tags.
5. Cite WHATWG URL in fix comments.