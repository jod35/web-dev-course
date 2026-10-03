# Logical Properties

Physical properties use left/right/top/bottom. Logical properties use inline/block, so they adapt when writing direction changes.

## Why

Physical:

```css
.card { margin-left: 1rem; padding-right: 1rem; }
```

Logical:

```css
.card { margin-inline-start: 1rem; padding-inline-end: 1rem; }
```

`inline` means along the text direction (horizontal for English, vertical for some scripts). `block` means perpendicular.

## Mapping

- `margin-left` → `margin-inline-start`
- `margin-right` → `margin-inline-end`
- `padding-top` → `padding-block-start`
- `padding-bottom` → `padding-block-end`
- `width` → `inline-size`
- `height` → `block-size`

```css
.container {
  inline-size: min(100% - 2rem, 70rem);
  margin-inline: auto; /* centers regardless of direction */
}
```

## When to use

- Use logical properties for spacing that should follow text flow, especially if your site may be translated.
- For a simple English-only page at MHSM, physical properties still work, but `margin-inline: auto` for centering is a good habit now.

```css
.card {
  padding-inline: 1rem;
  padding-block: 0.75rem;
  border-inline-start: 3px solid #0a58ca;
}
```

## Recap

| Physical | Logical |
|----------|---------|
| `margin-left` | `margin-inline-start` |
| `padding-right` | `padding-inline-end` |
| `width` | `inline-size` |
| `height` | `block-size` |

Prefer logical for margins, padding, and borders that should respect writing mode.
