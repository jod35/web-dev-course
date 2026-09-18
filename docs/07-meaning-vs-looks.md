# 07 - Meaning vs Looks (The Core Rule)

**Goal:** In this chapter you will learn the most important distinction in HTML text, which is that **semantic** elements describe meaning while visual elements only change appearance.

## The rule

> **When in doubt, go semantic.** Use `<strong>` instead of `<b>`, and use `<em>` instead of `<i>`.

Semantic elements tell **browsers, screen readers, and search engines** what the text *means*. Visual elements only change the rendering.

## Tag reference

### `<strong>` - importance

The `strong` element renders as bold text, **and** screen readers announce it as important. It also carries SEO weight:

```html
<p>Warning: <strong>Do not enter.</strong></p>
```

### `<b>` - visual bold only

The `b` element looks bold, but it means **nothing** to assistive technology or to search engines:

```html
<p>Use <b>bold</b> for looks alone.</p>
```

You should prefer `<strong>` unless you explicitly mean styling only, for example when you mark a product name inside a review.

### `<em>` - emphasis

The `em` element renders as italic text, **and** screen readers stress it when they read it aloud:

```html
<p>We are <em>closed</em> today.</p>
```

### `<i>` - visual italic only

```html
<p>The term <i>croissant</i> is French.</p>
```

Typical legitimate uses of `i` include foreign words, technical terms, and transliterations. When you want to place stress on a word, use `<em>` instead.

### `<mark>` - highlighted passage

The `mark` element marks text as **relevant**, in the same way a highlighter pen marks paper, and it shows a yellow background by default:

```html
<p>Result: <mark>passed</mark></p>
```

## Rules

- Nesting is acceptable, for example `<strong><em>both</em></strong>`, provided that you close the tags in reverse order.
- The `<b>` and `<i>` elements are not deprecated. They are simply free of meaning, so they should be used rarely and deliberately.

## Recap

| Tag | Meaning? | Renders |
|-----|----------|---------|
| `strong` | Important | Bold |
| `b` | None | Bold |
| `em` | Emphasis | Italic |
| `i` | None | Italic |
| `mark` | Relevant or highlighted | Highlighted |

**Next:** [08 - Code Family](08-code-family.md) · **Prev:** [06 - Combined](06-combined-structure.md)
