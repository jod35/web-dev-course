# 10 - Quotes: Block, Inline, Source

**Goal:** quote correctly with three tags, three jobs.

## Tag reference

### `<blockquote>`,long / block quote

A standalone quoted passage. Browsers indent it. `cite` holds the **source URL** (not shown, but machine-readable):

```html
<blockquote cite="https://example.com/interview">
  Fresh bread needs time, not shortcuts.
</blockquote>
```

### `<q>`,short inline quote

A quote inside a sentence. Browsers add the quotation marks **for you**,don't type them:

```html
<p>She said <q>Stay hungry.</q></p>
```

Renders as: She said "Stay hungry."

### `<cite>`,source title

The title of the **work** quoted,a book, article, talk. Never a person's name on its own:

```html
<cite>Whole Earth Catalog</cite>
```

Full pattern,quote plus its source:

```html
<blockquote cite="https://example.com/catalog">
  <p>Stay hungry, stay foolish.</p>
  <footer>— <cite>Whole Earth Catalog</cite></footer>
</blockquote>
```

## Gotchas

- `<q>` inside `<q>` nests with alternating quote marks,browsers handle it.
- `cite` the **work**, then name the author in plain text if needed: `<cite>Book</cite> by A. Uthor`.
- `cite` attribute (on `blockquote`) = URL for machines. `<cite>` element = title for humans. Don't confuse them.

## Recap

| Tag | Job | Marks added? |
|-----|-----|--------------|
| `blockquote` | Block quote | Indent, no quotes |
| `q` | Inline quote | Browser adds quotes |
| `cite` | Source title | None |

**Next:** [11,Special Blocks](11-special-blocks.md) · **Prev:** [09,Tiny Semantics](09-tiny-semantics.md)
