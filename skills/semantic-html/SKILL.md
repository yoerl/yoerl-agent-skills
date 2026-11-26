---
name: semantic-html
description: Applies semantic HTML elements correctly for accessibility and SEO. Use when refactoring markup, reviewing HTML/JSX structure, improving accessibility, or when the user asks for "semantic tags," "semantic HTML," "proper HTML structure," "accessibility markup," or "replace div/span with semantic elements."
metadata:
  version: 1.0.0
---

# Semantic HTML

Apply meaning-first HTML elements so structure is clear to assistive technologies and search engines. Prefer semantic elements over generic `<div>`/`<span>` when the meaning fits.

## When to Use This Skill

- Refactoring existing markup (e.g. div soup → semantic structure)
- Adding or editing page layout (header, main, nav, footer, sections)
- Implementing or reviewing accessible markup
- Choosing the right element for text (lists, quotes, emphasis, time, code)
- Forms, tables, media, and interactive UI (details/dialog)

## Core Rules

1. **Meaning over layout** — Use an element that describes the content's role. Use `<div>`/`<span>` only when no semantic element fits.
2. **One `<main>` per page** — Wraps the primary content; skip nav, header, footer, sidebars.
3. **Heading hierarchy** — Single `<h1>` per page; then `<h2>` → `<h3>` … without skipping levels.
4. **Landmarks** — Prefer `<header>`, `<nav>`, `<main>`, `<aside>`, `<footer>`, `<section>`, `<article>` so screen readers can jump by region.

## Element Choice Checklist

Before using `<div>` or `<span>`, check:

| If the content is… | Prefer this element |
|--------------------|----------------------|
| Page/section intro (logo, nav, search) | `<header>` |
| Primary content of the page | `<main>` |
| Navigation links (menu, TOC, pagination) | `<nav>` |
| Standalone piece (blog post, card, news item) | `<article>` |
| Thematic grouping with optional heading | `<section>` |
| Tangential content (sidebar, related links) | `<aside>` |
| Section/page footer (copyright, links) | `<footer>` |
| Contact info for nearest section/article | `<address>` |
| Single paragraph | `<p>` |
| Numbered list | `<ol>` + `<li>` |
| Bullet list | `<ul>` + `<li>` |
| Term + definition(s) | `<dl>`, `<dt>`, `<dd>` |
| Quoted block | `<blockquote>` (+ optional `<cite>`) |
| Short inline quote | `<q>` |
| Image/diagram with caption | `<figure>` + `<figcaption>` |
| Strong importance | `<strong>` |
| Emphasis (stress) | `<em>` |
| Time or date | `<time datetime="…">` |
| Code snippet | `<code>`; multi-line → `<pre><code>` |
| Keyboard input | `<kbd>` |
| Abbreviation (with full form) | `<abbr title="…">` |
| Link to another resource | `<a href="…">` |
| Button (submit, reset, custom action) | `<button>`; in form use `type="submit"` etc. |
| Form and controls | `<form>`, `<label>`, `<fieldset>`, `<legend>`, `<input>`, `<select>`, `<textarea>` |
| Expand/collapse block | `<details>` + `<summary>` |
| Modal/alert | `<dialog>` |
| Tabular data | `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`, `<caption>` |

## React/JSX Notes

- Use lowercase for HTML elements: `<main>`, `<section>`, `<article>`, etc.
- `class` → `className`; `for` → `htmlFor`.
- Fragment (`<>` / `<Fragment>`) does not change semantics; the first real child still defines the role (e.g. put `<main>` as direct child where appropriate).
- One root per component is fine; prefer a semantic wrapper (e.g. `<section>`, `<article>`) over a bare `<div>` when it matches the meaning.

## What to Avoid

- **No** presentational/legacy elements: `<center>`, `<font>`, `<big>`, `<marquee>`, `<strike>`, `<tt>`, etc. Use CSS or semantic alternatives.
- **No** multiple `<main>` on one page.
- **No** heading level jumps (e.g. `<h2>` next to `<h4>` with no `<h3>`).
- **No** `<div>`/`<span>` when a semantic element clearly fits (e.g. use `<nav>` for nav, `<button>` for buttons, `<time>` for dates).

## Quick Refactor Pattern

1. Identify each visual block (header, nav, main content, sidebars, footer).
2. Map each to a landmark: `<header>`, `<nav>`, `<main>`, `<aside>`, `<footer>`, or `<section>`/`<article>`.
3. Ensure one `<main>` and a single `<h1>`; fix heading order.
4. Replace generic wrappers for lists, quotes, figures, and forms with `<ul>`/`<ol>`, `<blockquote>`, `<figure>`, `<form>`, etc.
5. Use inline semantics where relevant: `<strong>`, `<em>`, `<time>`, `<code>`, `<abbr>`.