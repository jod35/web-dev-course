# Functions

Functions transform or calculate a value. You will use a handful often.

## Calc, min, max, clamp

```css
.container { width: min(100% - 2rem, 70rem); }
.card { width: clamp(220px, 50%, 360px); }
.hero { padding: clamp(1rem, 4vw, 3rem); }
```

- `calc()` — math: `calc(100% - 2rem)`
- `min()` — smallest of the list
- `max()` — largest
- `clamp(min, preferred, max)` — fluid with bounds, great for headings.

## Color functions

```css
.card { background: hsl(220 90% 41% / 0.9); }
.muted { color: color-mix(in srgb, currentColor 60%, transparent); }
```

## Other useful

```css
.card { background: var(--bg, #fff); } /* var with fallback */
.list { width: min(100%, 40rem); }
```

You can nest: `clamp(1rem, calc(1rem + 2vw), 2rem)`.

## When to use

- Fluid widths and hero padding: `min()`, `clamp()`
- Palette tweaks: `hsl()` with variable lightness
- Reuse: `var()`

## Recap

| Function | Use |
|----------|-----|
| `calc()` | Math |
| `min()`/`max()` | Bounds |
| `clamp()` | Fluid with min and max |
| `var()` | Custom property |
| `hsl()`/`rgb()` | Color |
