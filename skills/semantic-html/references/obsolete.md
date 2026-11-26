# Obsolete & presentational — forbidden list

**Reject** these in markup reviews. Cite [§16.2 Non-conforming features](https://html.spec.whatwg.org/multipage/obsolete.html#non-conforming-features).

## Entirely obsolete elements (must not use)

| Element | Replacement | Spec |
|---------|-------------|------|
| `applet` | `embed` or `object` | [§16.2](https://html.spec.whatwg.org/multipage/obsolete.html#non-conforming-features) |
| `acronym` | `abbr` | same |
| `bgsound` | `audio` | same |
| `dir` | `ul` | same |
| `frame`, `frameset`, `noframes` | `iframe` + CSS, or SSR | same |
| `isindex` | `form` + text control | same |
| `keygen` | Web Crypto API | same |
| `listing` | `pre` + `code` | same |
| `menuitem` | script + `contextmenu` event | same |
| `nextid` | GUIDs / `id` | same |
| `noembed` | `object` with fallback | same |
| `param` | `object` `data` attribute | same |
| `plaintext` | `text/plain` MIME type | same |
| `rb`, `rtc` | Ruby content directly in `ruby` | same |
| `strike` | `del` (edit) or `s` (strikethrough) | same |
| `xmp` | `pre` + `code` (escape `<` and `&`) | same |
| `basefont`, `big`, `blink`, `center`, `font`, `marquee`, `multicol`, `nobr`, `spacer`, `tt` | CSS + semantic elements (`kbd`, `var`, `code`, `samp`, `h1`–`h6`, `strong`, `mark`) | same |

## Presentational misuse

| Pattern | Fix |
|---------|-----|
| `div`/`span` styled as button | `<button type="button">` |
| `div`/`span` + `onClick` as link | `<a href="…">` |
| `table` for layout | CSS Grid / Flexbox |
| `br` for vertical spacing | CSS `margin` / `gap` |
| `h*` for font size only | CSS `font-size`; keep heading hierarchy |
| `b`/`i`/`u` when semantic fits | `strong`, `em`, `mark`, `cite`, etc. |

## Obsolete but conforming (warn, prefer modern)

| Feature | Prefer |
|---------|--------|
| `border` on `img` | CSS |
| `charset` on `script` | Omit (UTF-8 required) |
| `language` on `script` | Omit or `type` |
| `type="text/css"` on `style` | Omit attribute |
| `name` on `a` | `id` for fragments |

## Review procedure

1. Scan markup for forbidden element names.
2. Replace with spec-recommended alternative.
3. Cite WHATWG §16.2 URL in fix comment.