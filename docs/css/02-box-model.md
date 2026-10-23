# Box Model

Every element is a rectangular box. The box has four layers, from inside out:

```text
margin
┌─────────────────────────┐
│ border                  │
│ ┌─────────────────────┐ │
│ │ padding             │ │
│ │ ┌─────────────────┐ │ │
│ │ │ content         │ │ │
│ │ └─────────────────┘ │ │
│ └─────────────────────┘ │
└─────────────────────────┘
```

- **Content:** the text or image.
- **Padding:** space inside the border, around the content.
- **Border:** the edge of the box.
- **Margin:** space outside the border, between this box and its neighbours.

## Seeing the box model

```html
<div class="card">Hello</div>
```

```css
.card {
  width: 240px;
  padding: 16px;
  border: 2px solid #333;
  margin: 24px;
}
```

By default, `width` sets the content width only. The visible box is wider because padding and border are added:

```text
visible width = width + padding left + padding right + border left + border right
```

That default is called `content-box` and it catches almost everyone at least once.

## `box-sizing`

Set `box-sizing: border-box` once at the top of the stylesheet:

```css
* {
  box-sizing: border-box;
}

.card {
  width: 240px;
  padding: 16px;
  border: 2px solid #333;
}
```

Now `240px` includes the padding and border. This makes widths easier to reason about, especially in layouts.

## Padding and margin

- **Padding** is inside the box. The background colour covers it.
- **Margin** is outside the box. The background does not cover it.

```css
.card {
  padding: 1rem;
}

.card + .card {
  margin-top: 1rem;
}
```

Use padding when you want more space around the content inside a box. Use margin when you want space between boxes.

## Shorthand

```css
/* all four sides */
margin: 1rem;

/* vertical | horizontal */
padding: 0.5rem 1rem;

/* top | horizontal | bottom */
margin: 1rem 0 2rem;

/* top | right | bottom | left */
padding: 1rem 1.5rem 1rem 1.5rem;
```

The same pattern works for `border`, although you also need a width, style, and colour:

```css
.card {
  border: 1px solid #ddd;
}
```

## Margin collapse

Vertical margins between block elements can collapse. The larger margin wins:

```css
h2 {
  margin-bottom: 1rem;
}

p {
  margin-top: 1rem;
}
```

The gap between them is `1rem`, not `2rem`. This is normal. If you need exact spacing, use padding or `gap` in a flex or grid container.

## Try it

1. Add a card to a page with a background colour, padding, border, and margin.
2. Open the browser's developer tools and inspect the card.
3. Find the box model diagram in the styles panel. Hover over the content, padding, border, and margin areas to see them highlighted.
4. Change `box-sizing` from `border-box` to `content-box` and compare the visible width.
5. Put the setting back.

If the box is wider than you expected, check whether `box-sizing` is set.

Next: [Selectors](03-selectors.md)
