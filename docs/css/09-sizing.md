# Sizing

CSS can size things in absolute units, relative units, and units based on the viewport. Each is useful in different places.

## Pixels

```css
.card {
  width: 320px;
  border: 1px solid #ddd;
}
```

Use pixels for borders, hairlines, and small details. Avoid pixels for body text and large blocks of layout, because they do not respond to user font settings.

## `rem` and `em`

`rem` is relative to the root font size. `em` is relative to the current element's font size.

```css
html {
  font-size: 16px;
}

h1 {
  font-size: 2rem; /* 2 × 16px = 32px */
}

.card {
  padding: 1.5rem;
}

.small {
  font-size: 0.875em; /* relative to its parent */
}
```

Prefer `rem` for font sizes and spacing. It respects the reader's font settings and stays predictable. Use `em` when an element should scale with its own text, such as padding on a button.

## Percentages

```css
.container {
  width: min(100% - 2rem, 60rem);
}

.card {
  width: 50%;
}
```

Percentages are useful for fluid widths. `min(100% - 2rem, 60rem)` leaves space on small screens and sets a maximum width on large ones.

## Viewport units

```css
.banner {
  min-height: 60vh;
}

.full {
  min-height: 100dvh;
}
```

`vh` is a percentage of the viewport height. `dvh` accounts for mobile browser bars that appear and disappear. Use viewport units for large banners and full-screen sections, not for body text.

## Content-based sizing

```css
.card {
  width: fit-content;
}

.long {
  min-width: min-content;
}
```

`fit-content`, `min-content`, and `max-content` let the content decide the size. They are useful for menus, labels, and small components.

## Choosing a unit

| Need | Use |
|------|-----|
| Text and spacing | `rem` |
| Component padding | `rem` or `em` |
| Fluid widths | `%` with `min()` or `max()` |
| Borders and fine details | `px` |
| Full-screen sections | `vh` or `dvh` |

## Try it

1. Set the root font size to `16px`.
2. Make an `h1` `2rem` and a paragraph `1rem`.
3. Give a card `padding: 1.5rem` and a width of `min(100% - 2rem, 40rem)`.
4. Change the browser's default font size and check whether the page scales.
5. Replace one fixed pixel width with a percentage or `min()` and compare the layout at a narrow window width.

If text becomes tiny when you resize the window, you probably used a viewport unit for font size.

Next: [Layout](10-layout.md)
