# 07 - Meaning vs Looks (The Core Rule)

**Goal:** learn the most important distinction in HTML text: **semantic** elements describe meaning; visual elements only change looks.

## The rule

> **When in doubt, go semantic**,`<strong>` not `<b>`, `<em>` not `<i>`.

Semantic elements tell **browsers, screen readers, and search engines** what text *means*. Visual elements only change rendering.

## Tag reference

### `<strong>` - importance

Renders bold **and** is announced as important by screen readers. Carries SEO weight:

```html
<p>Warning: <strong>Do not enter.</strong></p>
```

### `<b>` - visual bold only

Looks bold. Means **nothing** to assistive tech or search:

```html
<p>Use <b>bold</b> for looks alone.</p>
```

Prefer `<strong>` unless you explicitly mean "styling only" (e.g., a product name in a review).

### `<em>` - emphasis

Renders italic **and** is stressed by screen readers:

```html
<p>We are <em>closed</em> today.</p>
```

### `<i>` - visual italic only

```html
<p>The term <i>croissant</i> is French.</p>
```

Typical legitimate uses: foreign words, technical terms, transliterations. For stress, use `<em>`.

### `<mark>` - highlighted passage

Marks text as **relevant**,like a highlighter pen (default yellow background):

```html
<p>Result: <mark>passed</mark></p>
```

## Rules

- Nesting is fine: `<strong><em>both</em></strong>`,close in reverse order.
- `<b>`/`<i>` are not deprecated,they are just meaning-free. Use them rarely and deliberately.

## Recap

| Tag | Meaning? | Renders |
|-----|----------|---------|
| `strong` | Important | Bold |
| `b` | None | Bold |
| `em` | Emphasis | Italic |
| `i` | None | Italic |
| `mark` | Relevant/hit | Highlighted |

**Next:** [08 - Code Family](08-code-family.md) · **Prev:** [06 - Combined](06-combined-structure.md)
