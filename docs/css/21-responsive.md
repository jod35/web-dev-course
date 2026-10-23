# Responsive Design

A page may be opened on a phone, tablet, or laptop. Responsive design means the same page stays readable on all of them.

## Start with fluid styles

Before adding media queries, make the content flexible:

```css
.container {
  width: min(100% - 2rem, 70rem);
  margin-inline: auto;
}

img,
video {
  max-width: 100%;
  height: auto;
}
```

The container keeps a little space at the edges on small screens and stops growing at `70rem` on large ones. Media elements shrink instead of overflowing.

## Media queries

Add a media query when the layout actually breaks:

```css
.layout {
  display: grid;
  gap: 1rem;
  grid-template-columns: 1fr;
}

@media (min-width: 640px) {
  .layout {
    grid-template-columns: 200px 1fr;
  }
}
```

This is mobile-first: the base styles are for the narrow layout, and the media query adds complexity as space grows.

Common breakpoints are around `640px` and `1024px`, but choose them by testing your content, not because a framework uses them.

## The viewport meta tag

Without this tag, mobile browsers zoom out and your media queries seem to be ignored:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

It belongs inside `<head>`.

## Text that scales

```css
h1 {
  font-size: clamp(1.5rem, 4vw, 2.5rem);
}
```

`clamp(min, preferred, max)` keeps a heading readable without adding a breakpoint for every size. Use it for large display text, not for every paragraph.

## Testing

- Use the browser's developer tools and drag the viewport width.
- Test with a real phone if possible.
- Check tap targets. Buttons and links should be at least `44px` tall.
- Zoom the page to 200% and check that text is still readable and does not require horizontal scrolling.
- Check that focus outlines are visible at every width.

## Try it

1. Build a page with a header, a main section, and two cards.
2. Make the cards stack by default.
3. Add a `min-width: 640px` media query that puts them side by side.
4. Change the heading size with `clamp()`.
5. Test at `320px`, `640px`, and `1280px`. Fix anything that overflows or becomes unreadable.

If the mobile layout looks zoomed out, check the viewport meta tag.

Next: [Functions](22-functions.md)
