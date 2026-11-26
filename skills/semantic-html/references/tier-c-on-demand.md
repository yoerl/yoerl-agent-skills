# Tier C — on-demand (rare elements)

Lookup when the specific UI pattern appears.

## Ruby & annotations

| Element | Use | Spec |
|---------|-----|------|
| `ruby` | Ruby annotation container | [#the-ruby-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-ruby-element) |
| `rt` | Ruby text | [#the-rt-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-rt-element) |
| `rp` | Fallback parentheses | [#the-rp-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-rp-element) |

## Abbreviations & definitions

| Element | Use | Spec |
|---------|-----|------|
| `abbr` | Abbreviation (`title` for expansion) | [#the-abbr-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-abbr-element) |
| `dfn` | Defining instance | [#the-dfn-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-dfn-element) |

## Data & machine-readable

| Element | Use | Spec |
|---------|-----|------|
| `data` | Machine-readable value (`value` attr) | [#the-data-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-data-element) |
| `time` | Date/time (`datetime`) | [#the-time-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-time-element) |

## Description lists

| Element | Use | Spec |
|---------|-----|------|
| `dl` | Association list | [#the-dl-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-dl-element) |
| `dt` | Term | [#the-dt-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-dt-element) |
| `dd` | Definition | [#the-dd-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-dd-element) |

## Edits & citations

| Element | Use | Spec |
|---------|-----|------|
| `del` / `ins` | Deleted / inserted text | [edits](https://html.spec.whatwg.org/multipage/edits.html) |
| `cite` | Title of referenced work | [#the-cite-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-cite-element) |

## Keyboard & sample output

| Element | Use |
|---------|-----|
| `kbd` | User keyboard input |
| `samp` | Program output |
| `var` | Variable name |

## Direction & typography

| Element | Use |
|---------|-----|
| `bdi` / `bdo` | Bi-directional isolation / override |
| `mark` | Highlighted text |
| `wbr` | Line-break opportunity |
| `sub` / `sup` | Subscript / superscript |
| `s` | Inaccurate/strikethrough (not edits — use `del`) |
| `b` / `i` / `u` / `small` | Styling hooks when no better semantic fits |

## Contact & address

| Element | Use | Spec |
|---------|-----|------|
| `address` | Contact info for section/article | [#the-address-element](https://html.spec.whatwg.org/multipage/sections.html#the-address-element) |

## Shadow DOM & custom

| Element | Use | Spec |
|---------|-----|------|
| `slot` | Shadow tree slot | [#the-slot-element](https://html.spec.whatwg.org/multipage/scripting.html#the-slot-element) |
| `template` | Inert template content | [#the-template-element](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element) |
| custom elements | Author-defined tags | [custom elements](https://html.spec.whatwg.org/multipage/custom-elements.html) |

## Head & metadata (rare in components)

| Element | Use |
|---------|-----|
| `base` | Base URL (one per doc, in `head`) |
| `link` | External resource link |
| `meta` | Metadata |
| `noscript` | Fallback when script disabled |

## Map & legacy patterns

| Element | Use |
|---------|-----|
| `map` + `area` | Client-side image map |
| `menu` | List of commands (prefer `ul` + buttons in most UIs) |
| `hgroup` | Multiple headings for one section |

Full inventory: [whatwg-elements-index.md](whatwg-elements-index.md)