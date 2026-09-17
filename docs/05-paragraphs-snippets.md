# 05,Paragraphs, Breaks, Rules (Syntax)

**Goal:** exact syntax for `p`, `br`, and `hr`.

## `<p>`,paragraph

Block of thought. Space above and below is automatic:

```html
<p>Fresh bread baked daily.</p>
```

## `<br>`,line break

Empty tag,**no closing tag**. Breaks the line inside the same paragraph:

```html
<p>Line one<br>Line two</p>
```

Renders as:

Line one
Line two

## `<hr>`,thematic break

Empty tag,**no closing tag**. Topic shift between blocks:

```html
<p>Menu</p>
<hr>
<p>Prices</p>
```

## Gotchas

- `<br>` inside headings is occasionally fine (a two-line title), but never use it for vertical spacing,that is CSS's job.
- Multiple `<hr>` in a row almost always means your sections need headings instead.

## Recap

| Tag | Closing tag? | Job |
|-----|--------------|-----|
| `p` | Yes `</p>` | Block of thought |
| `br` | No | Line break, same thought |
| `hr` | No | Thematic break |

**Next:** [06,Combined](06-combined-structure.md) · **Prev:** [04,What Are Paragraphs?](04-paragraphs.md)
