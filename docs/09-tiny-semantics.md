# 09 - Tiny Semantics - Big Meaning

**Goal:** In this chapter you will learn small inline tags which carry machine-readable meaning for abbreviations, dates, edits, and formulas.

## Tag reference

### `<abbr>` - abbreviation

The `title` attribute **must** hold the full form of the abbreviation. Browsers show it as a tooltip, and screen readers announce it:

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

```html
<abbr title="Cascading Style Sheets">CSS</abbr>
```

An `<abbr>` element without a `title` attribute is pointless, so never omit it.

### `<time>` - date / time

The `datetime` attribute holds the **machine-readable** value in ISO format, while the element content holds the human reading:

```html
<time datetime="2026-09-16">Sept 16, 2026</time>
```

```html
<time datetime="07:00">7am</time>
```

Search engines and calendars can parse the `datetime` value, while they cannot parse plain text.

### `<del>` / `<ins>` - edits

The `del` and `ins` elements mark deleted and inserted text. Browsers strike through `<del>` content and underline `<ins>` content, **and** both elements carry meaning because they record the history of a document instead of adding decoration:

```html
<del>Old price $5</del> <ins>New price $4</ins>
```

```html
<p><del>closed</del> <ins>open</ins> on Sundays</p>
```

The optional `cite` and `datetime` attributes record the source and the date of the change:

```html
<del cite="https://example.com/menu-v2" datetime="2026-09-01">Old menu</del>
```

### `<sub>` / `<sup>` - subscript / superscript

The `sub` and `sup` elements mark formulas and footnotes, and they must **not** be used for generic small or raised styling:

```html
<p>H<sub>2</sub>O and x<sup>2</sup></p>
```

## Rules

- The `<del>` and `<ins>` elements can wrap block content such as whole paragraphs, not only single words.
- For footnote markers, pair the `<sup>` element with a matching link, as explained in Chapter 12.

## Recap

| Tag | Key attribute | Example |
|-----|---------------|---------|
| `abbr` | `title`, required in practice | `<abbr title="…">HTML</abbr>` |
| `time` | `datetime` in ISO format | `<time datetime="2026-09-16">…</time>` |
| `del` / `ins` | `cite` and `datetime`, both optional | `<del>old</del> <ins>new</ins>` |
| `sub` / `sup` | None | `H<sub>2</sub>O`, `x<sup>2</sup>` |

**Next:** [10 - Quotes](10-quotes.md) · **Prev:** [08 - Code Family](08-code-family.md)
