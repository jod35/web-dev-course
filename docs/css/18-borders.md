# Borders

Borders draw a line around the box. They have width, style, and color.

## Shorthand

```css
.card { border: 1px solid #ddd; }
```

Equivalent to:

```css
.card {
  border-width: 1px;
  border-style: solid;
  border-color: #ddd;
}
```

## Sides and logical sides

```css
.card { border-top: 2px solid #0a58ca; }
.card { border-inline-start: 3px solid #0a58ca; } /* logical, follows writing mode */
```

## Radius

```css
.card { border-radius: 0.5rem; }
.avatar { border-radius: 50%; } /* circle if square */
.pill { border-radius: 999px; }
```

Individual corners:

```css
.card { border-top-left-radius: 0.5rem; border-top-right-radius: 0.5rem; }
```

Or using logical:

```css
.card { border-start-start-radius: 0.5rem; }
```

## Outline vs border

- **Border** — takes space, affects layout.
- **Outline** — draws outside, no layout shift, great for focus:

```css
:focus-visible { outline: 2px solid #333; outline-offset: 2px; }
```

## Example: subtle card

```css
.card {
  border: 1px solid #e5e7eb;
  border-radius: 0.5rem;
}
.card:hover { border-color: #d1d5db; }
```

## Recap

| Property | Example |
|----------|---------|
| `border` | `1px solid #ddd` |
| `border-radius` | `0.5rem`, `50%`, `999px` |
| Logical | `border-inline-start` |
| Focus | `outline` with `outline-offset` |
