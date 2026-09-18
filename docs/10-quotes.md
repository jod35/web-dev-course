# 10 - Quotes: Block, Inline, Source

**Goal:** In this chapter you will learn how to quote correctly with three tags which perform three different jobs.

## Tag reference

### `<blockquote>` - long / block quote

The `blockquote` element holds a standalone quoted passage. Browsers indent the passage, and the `cite` attribute holds the **source URL**, which remains machine-readable and is not displayed:

```html
<blockquote cite="https://example.com/interview">
  Fresh bread needs time, not shortcuts.
</blockquote>
```

### `<q>` - short inline quote

The `q` element holds a short quote inside a sentence. Browsers add the quotation marks **for you**, so do not type them yourself:

```html
<p>She said <q>Stay hungry.</q></p>
```

It renders as: She said "Stay hungry."

### `<cite>` - source title

The `cite` element holds the title of the **work** which has been quoted, such as a book, an article, or a talk. It must never hold a person's name on its own:

```html
<cite>Whole Earth Catalog</cite>
```

The following example shows the complete pattern with a quote and its source:

```html
<blockquote cite="https://example.com/catalog">
  <p>Stay hungry, stay foolish.</p>
  <footer>— <cite>Whole Earth Catalog</cite></footer>
</blockquote>
```

## Rules

- A `<q>` element can sit inside another `<q>` element, and browsers handle the alternating quote marks.
- Cite the **work** first, and then name the author in plain text when that detail is needed, for example `<cite>Book</cite> by A. Uthor`.
- The `cite` attribute on `blockquote` is a URL for machines, while the `<cite>` element is a title for humans, so the two must not be confused.

## Recap

| Tag | Job | Marks added? |
|-----|-----|--------------|
| `blockquote` | Block quote | Indent, no quotes |
| `q` | Inline quote | Browser adds quotes |
| `cite` | Source title | None |

**Next:** [11 - Special Blocks](11-special-blocks.md) · **Prev:** [09 - Tiny Semantics](09-tiny-semantics.md)
