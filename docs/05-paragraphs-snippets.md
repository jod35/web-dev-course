# 05 - Paragraphs, Breaks, Rules (Syntax)

**Goal:** In this chapter you will learn the exact syntax for `p`, `br`, and `hr`.

## `<p>` - paragraph

The `p` element defines a block of thought. The space above and below each paragraph is added automatically:

```html
<p>Fresh bread baked daily.</p>
```

## `<br>` - line break

The `br` element is an empty tag, so it has **no closing tag**. It breaks the line inside the same paragraph:

```html
<p>Line one<br>Line two</p>
```

It renders as:

Line one
Line two

## `<hr>` - thematic break

The `hr` element is an empty tag, so it has **no closing tag**. It signals a shift in topic between blocks:

```html
<p>Menu</p>
<hr>
<p>Prices</p>
```

## Rules

- A `<br>` element inside a heading is occasionally acceptable, for example in a two-line title, but it must never be used for vertical spacing, because that spacing is the job of CSS.
- Multiple `<hr>` elements in a row almost always indicate that the sections need headings instead.

## Recap

| Tag | Closing tag? | Job |
|-----|--------------|-----|
| `p` | Yes, `</p>` | Block of thought |
| `br` | No | Line break within the same thought |
| `hr` | No | Thematic break |

**Next:** [06 - Combined](06-combined-structure.md) · **Prev:** [04 - What Are Paragraphs?](04-paragraphs.md)
