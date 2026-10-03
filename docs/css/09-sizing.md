# Sizing

How big is a box? CSS has absolute and relative ways to answer that.

## Pixels

```css
.card { width: 320px; border: 1px solid #ddd; }
```

Use `px` for borders, hairlines, and tiny details. Avoid `px` for main text sizes.

## Relative to font: rem and em

```css
html { font-size: 16px; }
h1 { font-size: 2rem; }   /* 2 × root = 32px */
.card { padding: 1.5rem; }
.small { font-size: 0.875em; } /* relative to its parent */
```

Prefer `rem` for font sizes and spacing. It respects user settings and stays predictable. `em` is useful for a small element that should scale with its parent.

## Relative to parent: percent

```css
.container { width: min(100% - 2rem, 60rem); }
.card { width: 50%; }
```

`%` is great for fluid widths. `min(100% - 2rem, 60rem)` gives breathing room on small screens and a max width on large screens.

## Viewport units

```css
.hero { min-height: 60vh; }
.full { min-height: 100dvh; } /* dynamic viewport, handles mobile bars */
```

Use viewport units for hero sections, not for body text.

## Intrinsics

```css
.card { width: fit-content; }
.long { min-width: min-content; }
```

`fit-content`, `min-content`, `max-content` let the content decide the size. Handy for badges and menus.

## Choosing

- Text and vertical spacing: `rem`
- Component padding and gaps: `rem`
- Widths that flex: `%` or `rem` with `min()`/`max()`
- Tiny lines: `px`
- Heroes: `vh`/`dvh`

## Recap

| Need | Use |
|------|-----|
| Text and spacing | `rem` |
| Widths | `%` with `min()` |
| Tiny details | `px` |
| Hero height | `vh`/`dvh` |
