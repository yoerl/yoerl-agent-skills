# semantic-html references

Hybrid tiered reference for **WHATWG HTML Living Standard** conformance.

- **Normative spec:** [HTML Living Standard](https://html.spec.whatwg.org/multipage/)
- **Spec snapshot:** 2026-11-26

## How to use

| Tier | File | When |
|------|------|------|
| **Daily** | [tier-a-daily.md](tier-a-daily.md) | Every markup task — mandatory checks |
| **On-demand B** | [tier-b-on-demand.md](tier-b-on-demand.md) | Forms, tables, media, interactive UI |
| **On-demand C** | [tier-c-on-demand.md](tier-c-on-demand.md) | Rare elements — lookup when UI needs them |
| **Catalog** | [whatwg-elements-index.md](whatwg-elements-index.md) | Full element inventory + spec fragment links |
| **Nesting** | [content-models.md](content-models.md) | Flow / phrasing / sectioning — invalid nesting rules |
| **Forbidden** | [obsolete.md](obsolete.md) | Obsolete & presentational elements — reject |
| **JSX** | [react-notes.md](react-notes.md) | React/JSX attribute and shell caveats |

## Installed path

After `npx skills add …@semantic-html`, references live at:

```
.agents/skills/semantic-html/references/
```

## Dispute resolution

When element choice or nesting is disputed, cite the **WHATWG multipage section URL** from the catalog — not blog posts or MDN alone.

## SVG & MathML

`svg` and `math` are listed in the element index with one-line notes. Deep markup rules live in [SVG](https://www.w3.org/TR/SVG2/) and [MathML](https://www.w3.org/TR/MathML4/) — not covered here.