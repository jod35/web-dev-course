# Paragraphs, Breaks, Rules (Syntax)

Here's the exact syntax for `p`, `br`, and `hr`, nothing extra.

## `<p>`: paragraph

`p` wraps a block of thought. Spacing above and below is added for you:

```html
<p>Fresh bread baked daily.</p>
```

## `<br>`: line break

Empty tag, so **no closing tag**. It just breaks the line inside the same paragraph:

```html
<p>Line one<br>Line two</p>
```

Renders as:

Line one
Line two

## `<hr>`: thematic break

Also an empty tag, **no closing tag**. It signals a shift in topic between blocks:

```html
<p>Menu</p>
<hr>
<p>Prices</p>
```

## A couple of guardrails

- A `<br>` inside a heading can be okay for a two-line title, but never use it for vertical spacing: that's what CSS margins are for.
- Seeing several `<hr>`s in a row? That's usually a hint you actually want headings instead.

## Recap

| Tag | Closing tag? | Job |
|-----|--------------|-----|
| `p` | Yes, `</p>` | Block of thought |
| `br` | No | Line break within the same thought |
| `hr` | No | Thematic break |
