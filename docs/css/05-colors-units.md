# Colors & Units

CSS needs you to say how big and what color. There are a few good ways for each.

## Colors

**Hex — compact, common:**

```css
.card { background: #0a58ca; color: #ffffff; }
```

**RGB — explicit, easy to add alpha:**

```css
.card { background: rgb(10 88 202); }
.card { background: rgba(10 88 202 / 0.8); }
```

**HSL — intuitive to tweak:**

```css
/* hue 220, saturation 90%, lightness 41% */
.btn { background: hsl(220 90% 41%); }
```

Pick one and stay consistent. For this course we will use `hex` for static values and `hsl` when we want to adjust lightness.

**CurrentColor and transparent:**

```css
.card { border: 1px solid currentColor; } /* uses the text color */
.ghost { background: transparent; }
```

## Units

**Absolute — `px`:**

```css
.card { width: 320px; border: 1px solid #ddd; }
```

Use `px` for borders and hairlines, not for main text sizes.

**Relative to font — `rem` and `em`:**

```css
html { font-size: 16px; }
h1 { font-size: 2rem; }   /* 2 × root = 32px */
.card { padding: 1.5rem; }
.small { font-size: 0.875em; } /* relative to parent */
```

Prefer `rem` for font sizes and spacing. It scales with user settings and stays predictable.

**Relative to parent — `%`:**

```css
.container { width: min(100% - 2rem, 60rem); }
.card { width: 50%; }
```

**Viewport — `vw`, `vh`, `dvh`:**

```css
.hero { min-height: 60vh; }
```

Use viewport units for hero sections, not for body text.

## Choosing

- Text size and vertical spacing: `rem`
- Component padding and gaps: `rem`
- Widths that should flex: `%` or `rem` with `min()`/`max()`
- Borders, shadows, tiny details: `px`
- Colors: `hex` or `hsl`, one palette consistently

Example palette as CSS variables (you will use these later):

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

## Recap

| Need | Use |
|------|-----|
| Text and spacing | `rem` |
| Widths | `%`, `rem` with `min()` |
| Tiny lines | `px` |
| Colors | `hex`/`hsl` consistently |
