# Inheritance

Some CSS properties pass from a parent element to its children. Others do not.

## What inherits

Text-related properties usually inherit:

- `color`
- `font-family`
- `font-size`
- `line-height`
- `text-align`

Box-related properties usually do not inherit:

- `margin`
- `padding`
- `border`
- `background`
- `width`
- `display`

You do not need to memorise the full list. Remember the pattern: text styles flow down, box styles do not.

```css
body {
  color: #222;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
}
```

A paragraph inside `<body>` gets the colour, font, and line height without extra rules. A `<div>` does not inherit the body's padding or background.

## Controlling inheritance

Use `inherit` when you want a child to take the parent's value explicitly:

```css
a {
  color: inherit;
}
```

This makes a link use the surrounding text colour instead of the browser's default blue.

Other global values:

- `initial` resets the property to its browser default.
- `unset` inherits when the property normally inherits, otherwise resets it.

```css
.card {
  color: #333;
}

.card a {
  color: inherit;
}
```

## Why it matters

Set text styles high in the document and box styles on the component:

```css
body {
  color: #222;
  font-family: system-ui, sans-serif;
}

.card {
  padding: 1rem;
  border: 1px solid #ddd;
  background: #fff;
}
```

Then the card's text inherits the body styles, while its padding and border stay local to the card. You avoid repeating font declarations on every element.

## Try it

1. Set `color` and `font-family` on `body`.
2. Add a paragraph and a link inside it. Which styles does each inherit?
3. Add a `.card` with padding, border, and background. Check whether the paragraph inside inherits those box styles.
4. Add `.card a { color: inherit; }` and compare the link with the default link colour.
5. Try `initial` and `unset` on one property and observe the difference.

If a text style is missing, check whether it was set on an ancestor or on the element itself.

Next: [Color](08-color.md)
