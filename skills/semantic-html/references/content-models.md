# Content models — nesting rules

Summary of WHATWG content categories. When in doubt, cite the spec link.

**Spec:** [Element content categories](https://html.spec.whatwg.org/multipage/dom.html#kinds-of-content)

## Categories (quick)

| Category | Meaning | Example elements |
|----------|---------|------------------|
| **Metadata** | Document metadata; not rendered in body flow | `head`, `meta`, `link`, `style`, `script`, `title`, `base`, `template` |
| **Flow** | Default body content; blocks and inline mixed | `div`, `p`, `article`, `ul`, `section`, `button` |
| **Sectioning** | Creates document outline section | `article`, `aside`, `nav`, `section` |
| **Heading** | Section heading | `h1`–`h6`, `hgroup` |
| **Phrasing** | Inline / run-in content | `span`, `a`, `strong`, `code`, `img`, `input` |
| **Embedded** | External resource | `img`, `video`, `audio`, `iframe`, `canvas`, `svg`, `math` |
| **Interactive** | User interaction | `a` (with `href`), `button`, `input`, `select`, `textarea`, `details`, `label` |
| **Palpable** | Has box or text content authors expect to see | Most flow elements with visible content |

## Common invalid nesting

| Parent | Invalid child | Why | Spec |
|--------|---------------|-----|------|
| `p` | `p`, `div`, `ul`, `h1`–`h6`, `section` | `p` only allows phrasing | [#the-p-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-p-element) |
| `a` | interactive element (`button`, `a`, `input`) | No interactive descendants in `a` | [#the-a-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-a-element) |
| `button` | `button`, `a` (with href), `input` | No interactive descendants | [#the-button-element](https://html.spec.whatwg.org/multipage/form-elements.html#the-button-element) |
| `span` | `div`, `p`, `ul` | `span` is phrasing only | [#the-span-element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-span-element) |
| `ul` / `ol` | raw text (not in `li`) | Only `li` (+ script-supporting) | [#the-ul-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-ul-element) |
| `table` | bare `tr` without `thead`/`tbody`/`tfoot` | Rows go in section elements or directly (implicit tbody) | [#the-table-element](https://html.spec.whatwg.org/multipage/tables.html#the-table-element) |
| `main` | nested `main` | One `main` per document (hierarchically correct) | [#the-main-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-main-element) |
| `address` | `article`, `section`, headings, nested `address` | Limited flow model | [#the-address-element](https://html.spec.whatwg.org/multipage/sections.html#the-address-element) |
| `label` | `label` | No nested labels | [#the-label-element](https://html.spec.whatwg.org/multipage/form-elements.html#the-label-element) |
| `figcaption` | `figcaption` ancestor | One caption per `figure` | [#the-figcaption-element](https://html.spec.whatwg.org/multipage/grouping-content.html#the-figcaption-element) |
| heading (`h1`–`h6`) | heading without intervening content | Don't skip levels for outline | [#outline](https://html.spec.whatwg.org/multipage/sections.html#headings-and-sections) |

## Transparent & text models

Some elements have **transparent** content models (`a`, `ins`, `del`, `object`): they inherit the parent's restrictions. Validate as if the children were direct children of the grandparent.

## Validation procedure

1. Identify parent element's allowed children (catalog or spec link).
2. Check child against parent's content model.
3. If transparent, re-check against grandparent.
4. Cite spec URL in review comment when fixing.