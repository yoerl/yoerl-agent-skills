# Tier A — daily mandatory checks

Apply on **every** markup task. ~40 frequent elements.

## Landmarks & outline

| Check | Rule | Spec |
|-------|------|------|
| Single `main` | One hierarchically correct `main` per document | [#the-main-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-main-element) |
| Single `h1` | One top-level heading per page | [#outline](https://html.spec.whatwg.org/multipage/sections.html#headings-and-sections) |
| Heading order | `h1` → `h2` → `h3`… no skipped levels | [#outline](https://html.spec.whatwg.org/multipage/sections.html#headings-and-sections) |
| Landmarks | `header`, `nav`, `main`, `aside`, `footer` for page regions | [sections](https://html.spec.whatwg.org/multipage/sections.html) |

## Sectioning & grouping

| Element | Use when |
|---------|----------|
| `header` | Introductory content for page or section |
| `nav` | Block of navigation links |
| `main` | Dominant content of the document |
| `aside` | Tangentially related content (sidebar) |
| `footer` | Footer for nearest sectioning root or section |
| `section` | Thematic grouping with heading |
| `article` | Self-contained composition (post, card, widget) |
| `div` | **Only** when no semantic element fits |

## Headings & text

| Element | Use when |
|---------|----------|
| `h1`–`h6` | Section headings (not for sizing) |
| `p` | Paragraph |
| `ul` / `ol` / `li` | Lists |
| `blockquote` / `q` | Block / inline quotation |
| `strong` / `em` | Importance / stress emphasis |
| `time` | Date or time (`datetime` attr) |
| `code` / `pre` | Inline code / preformatted block |

## Links & controls

| Element | Use when |
|---------|----------|
| `a` | Navigation to another resource (`href`) |
| `button` | Action control (`type="button"` default for non-submit) |
| **Not** `div`/`span` + `onClick` for links or buttons | Use `a` or `button` |

## Media & figures

| Element | Use when |
|---------|----------|
| `img` | Image (`alt` required unless decorative) |
| `figure` + `figcaption` | Image/diagram with caption |

## Forms (basics)

| Element | Use when |
|---------|----------|
| `form` | User-submittable form |
| `label` | Caption (`for` ↔ control `id`) |
| `input` | Single-line control (right `type`) |
| `textarea` | Multi-line text |
| `select` / `option` | List box |

## Daily reject list

- `div`/`span` where `nav`, `button`, `a`, `ul`, `p`, `section` fits
- Multiple `main`
- Presentational/obsolete tags → see [obsolete.md](obsolete.md)