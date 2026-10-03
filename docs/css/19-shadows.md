# Shadows

Shadows add depth. Two properties: `box-shadow` for boxes, `text-shadow` for text.

## Box shadow

```css
.card {
  box-shadow: 0 1px 3px rgba(0 0 0 / 0.12);
}
```

Syntax: `offset-x offset-y blur spread color`. You rarely need spread.

```css
/* soft, larger shadow */
.card-elevated {
  box-shadow: 0 4px 12px rgba(0 0 0 / 0.12);
}

/* multiple layers, more natural */
.card-layered {
  box-shadow:
    0 1px 2px rgba(0 0 0 / 0.08),
    0 4px 12px rgba(0 0 0 / 0.10);
}
```

## Inset and color

```css
.pressed { box-shadow: inset 0 2px 4px rgba(0 0 0 / 0.12); }
.brand-shadow { box-shadow: 0 4px 12px hsl(220 90% 41% / 0.25); }
```

## Text shadow

```css
.hero-title { text-shadow: 0 1px 2px rgba(0 0 0 / 0.25); }
```

Use sparingly, usually just to lift text off a photo.

## Where to use

- Cards, dialogs, dropdowns: `box-shadow`
- Focus on photos: `text-shadow`
- Define as variables for consistency:

```css
:root {
  --shadow-sm: 0 1px 2px rgba(0 0 0 / 0.08);
  --shadow-md: 0 4px 12px rgba(0 0 0 / 0.12);
}
.card { box-shadow: var(--shadow-sm); }
.card:hover { box-shadow: var(--shadow-md); }
```

## Recap

| Need | Write |
|------|-------|
| Soft box | `box-shadow: 0 1px 3px rgba(... / 0.12)` |
| Layered | Two shadows, comma separated |
| Text lift | `text-shadow: 0 1px 2px rgba(...)` |
