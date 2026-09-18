# 09 - Tiny Semantics - Big Meaning

**Goal:** small inline tags that carry machine-readable meaning: abbreviations, dates, edits, formulas.

## Tag reference

### `<abbr>` - abbreviation

`title` **must** hold the full form,shown as a tooltip and announced by screen readers:

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

```html
<abbr title="Cascading Style Sheets">CSS</abbr>
```

An `<abbr>` without `title` is pointless,never omit it.

### `<time>`,date / time

`datetime` holds the **machine-readable** value (ISO format); the content is the human reading:

```html
<time datetime="2026-09-16">Sept 16, 2026</time>
```

```html
<time datetime="07:00">7am</time>
```

Search engines and calendars can parse `datetime`,plain text they cannot.

### `<del>` / `<ins>` - edits

Deleted and inserted text. Browsers strike through `<del>` and underline `<ins>` **with meaning** (a document history, not decoration):

```html
<del>Old price $5</del> <ins>New price $4</ins>
```

```html
<p><del>closed</del> <ins>open</ins> on Sundays</p>
```

Optional `cite` (source URL) and `datetime` attributes record *why/when*:

```html
<del cite="https://example.com/menu-v2" datetime="2026-09-01">Old menu</del>
```

### `<sub>` / `<sup>` - subscript / superscript

Formulas and footnotes,**not** generic small/raised styling:

```html
<p>H<sub>2</sub>O and x<sup>2</sup></p>
```

## Rules

- `<del>`/`<ins>` can wrap block content too (whole paragraphs), not just words.
- For footnote markers pair `<sup>` with a matching link (Chapter 12).

## Recap

| Tag | Key attribute | Example |
|-----|---------------|---------|
| `abbr` | `title` (required in practice) | `<abbr title="…">HTML</abbr>` |
| `time` | `datetime` (ISO) | `<time datetime="2026-09-16">…</time>` |
| `del` / `ins` | `cite`, `datetime` (optional) | `<del>old</del> <ins>new</ins>` |
| `sub` / `sup` |,| `H<sub>2</sub>O`, `x<sup>2</sup>` |

**Next:** [10 - Quotes](10-quotes.md) · **Prev:** [08 - Code Family](08-code-family.md)
