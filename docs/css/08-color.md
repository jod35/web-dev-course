# Color

CSS gives you several ways to say what color. Pick one palette and stay consistent.

## Hex

Compact, common for static values:

```css
.card { background: #0a58ca; color: #ffffff; }
```

Shorthand when pairs repeat: `#fff` is `#ffffff`.

## RGB

Explicit, easy to add alpha:

```css
.card { background: rgb(10 88 202); }
.card { background: rgb(10 88 202 / 0.8); } /* 80% opacity, new syntax */
```

## HSL

Hue, saturation, lightness. Intuitive to tweak:

```css
/* hue 220, saturation 90%, lightness 41% */
.btn { background: hsl(220 90% 41%); }
/* lighter */
.btn:hover { background: hsl(220 90% 48%); }
```

If you need to make a color lighter or darker, `hsl` is easiest.

## CurrentColor and transparent

```css
.card { border: 1px solid currentColor; } /* border uses the text color */
.ghost { background: transparent; }
```

`currentColor` keeps border and text in sync.

## A palette as variables

Define once, reuse:

```css
:root {
  --bg: #ffffff;
  --text: #1a1a1a;
  --muted: #6b7280;
  --primary: hsl(220 90% 41%);
}
body { color: var(--text); background: var(--bg); }
.btn-primary { background: var(--primary); color: #fff; }
```

You will meet custom properties properly later, but this is where they shine for color.

## Recap

| Format | When to use |
|--------|-------------|
| `hex` | Static palette |
| `rgb`/`rgba` | When you need alpha with explicit channels |
| `hsl` | When you will lighten or darken |
| `currentColor` | Keep border synced to text |
