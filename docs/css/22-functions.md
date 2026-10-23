# Functions

CSS functions calculate or transform values. You will use a few of them often.

## `calc()`, `min()`, `max()`, and `clamp()`

```css
.container {
  width: min(100% - 2rem, 70rem);
}

.card {
  width: clamp(220px, 50%, 360px);
}

.banner {
  padding: clamp(1rem, 4vw, 3rem);
}
```

- `calc()` performs arithmetic: `calc(100% - 2rem)`.
- `min()` returns the smallest value in a list.
- `max()` returns the largest value.
- `clamp(min, preferred, max)` keeps a value between a minimum and a maximum.

`clamp()` is useful for fluid headings and padding. It is not a replacement for every media query.

## Colour functions

```css
.card {
  background: hsl(220 90% 41% / 0.9);
}

.muted {
  color: color-mix(in srgb, currentColor 60%, transparent);
}
```

`hsl()` is convenient for adjusting lightness. `color-mix()` mixes two colours. Check browser support before relying on a newer function for essential content.

## Custom property functions

```css
.card {
  background: var(--bg, #fff);
}

.list {
  width: min(100%, 40rem);
}
```

`var()` reads a custom property and can provide a fallback.

Functions can be nested:

```css
.title {
  font-size: clamp(1rem, calc(1rem + 2vw), 2rem);
}
```

## Try it

1. Build a container with `min(100% - 2rem, 70rem)`.
2. Give a heading a `clamp()` size and test it at narrow and wide widths.
3. Use `calc()` to make a sidebar slightly narrower than a fixed value.
4. Define a custom property and read it with `var()`.
5. Use `color-mix()` for a muted text colour and check the contrast.

If a function does not work, check the parentheses, commas, and units. `min(100% - 2rem 70rem)` is invalid because the two arguments are not separated by a comma.

Next: [Practice: Build a Page](23-practice.md)
