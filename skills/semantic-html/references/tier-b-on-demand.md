# Tier B — on-demand (forms, tables, media, interactive)

Open when the UI needs these patterns.

## Forms — validation & association

| Topic | Rule | Spec |
|-------|------|------|
| `label` + `for` | Associates caption with control | [#the-label-element](https://html.spec.whatwg.org/multipage/form-elements.html#the-label-element) |
| `fieldset` + `legend` | Group related controls | [#the-fieldset-element](https://html.spec.whatwg.org/multipage/form-elements.html#the-fieldset-element) |
| `required` | Boolean on submittable controls | [attr-required](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-required) |
| `pattern` | Regex constraint on text `input` | [attr-pattern](https://html.spec.whatwg.org/multipage/input.html#attr-input-pattern) |
| `min` / `max` / `step` | Numeric/date constraints | [the input element](https://html.spec.whatwg.org/multipage/input.html#the-input-element) |
| `aria-*` | Use when native semantics insufficient — prefer native first | [ARIA in HTML](https://www.w3.org/TR/html-aria/) |
| `datalist` + `list` | Combobox suggestions | [#the-datalist-element](https://html.spec.whatwg.org/multipage/form-elements.html#the-datalist-element) |
| `output` | Calculated result (`for` lists input ids) | [#the-output-element](https://html.spec.whatwg.org/multipage/form-elements.html#the-output-element) |

## Tables

| Element | Role |
|---------|------|
| `table` | Tabular data (not layout) |
| `caption` | Table title |
| `thead` / `tbody` / `tfoot` | Row groups |
| `tr` | Row |
| `th` | Header cell (`scope="col"` / `"row"`) |
| `td` | Data cell |
| `colgroup` / `col` | Column styling |

**Spec:** [Tables](https://html.spec.whatwg.org/multipage/tables.html)

## Media

| Element | Use |
|---------|-----|
| `picture` + `source` + `img` | Responsive images / art direction |
| `video` + `source` + `track` | Video with captions/subtitles |
| `audio` + `source` | Audio playback |
| `track` | Timed text (`kind="captions"` for a11y) |

**Spec:** [Embedded content](https://html.spec.whatwg.org/multipage/embedded-content.html)

## Interactive

| Element | Use |
|---------|-----|
| `details` + `summary` | Disclosure widget (no JS needed) |
| `dialog` | Modal / dialog (`open`, `showModal()`, focus trap) |
| `search` | Search form region (landmark) |
| `meter` / `progress` | Gauge / progress bar |

**Nesting:** See [content-models.md](content-models.md) — `details` needs `summary` first; `dialog` accepts flow content.