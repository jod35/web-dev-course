# Responsive Design

Your page will be opened on phones, tablets, and laptops. Responsive design means it reads well on all of them without building separate pages.

## Fluid first

Before any media query, make things fluid:

```css
.container {
  width: min(100% - 2rem, 70rem);
  margin-inline: auto; /* centers it */
}
img, video { max-width: 100%; height: auto; }
```

`min(100% - 2rem, 70rem)` gives you breathing room on small screens and a max width on large ones.

## Media queries

Add adjustments where the layout actually breaks, usually around `640px` and `1024px`:

```css
.layout {
  display: grid;
  gap: 1rem;
}
/* mobile: single column by default */
.layout { grid-template-columns: 1fr; }

/* tablet and up: two columns */
@media (min-width: 640px) {
  .layout { grid-template-columns: 200px 1fr; }
}
```

Mobile-first means base styles are for small screens, media queries add complexity as space grows. It keeps CSS smaller and more predictable.

## Viewport meta

Without this, mobile browsers zoom out and your media queries seem ignored:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

You already have it in the HTML template. Do not remove it.

## Typography that scales

```css
h1 { font-size: clamp(1.5rem, 4vw, 2.5rem); }
```

`clamp(min, preferred, max)` keeps headings readable without a pile of breakpoints. Use it for hero titles, not for every `p`.

## Testing

- In the browser, use DevTools device toolbar and drag the width.
- Test real tap targets: buttons at least `44px` tall.
- Check text at `200%` zoom — it should still be readable without horizontal scroll.

## Recap

| Habit | Why |
|-------|-----|
| Fluid container + `max-width: 100%` on media | No overflow on small screens |
| Mobile-first + `min-width` queries | Simpler overrides |
| `meta viewport` present | Media queries actually work |
| `clamp()` for hero type | Smooth scaling |
