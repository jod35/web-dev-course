# Logical Properties

Physical properties use `left`, `right`, `top`, and `bottom`. Logical properties use `inline` and `block`, so they adapt when the writing direction changes.

## Why use them

Physical:

```css
.card {
  margin-left: 1rem;
  padding-right: 1rem;
}
```

Logical:

```css
.card {
  margin-inline-start: 1rem;
  padding-inline-end: 1rem;
}
```

`inline` means along the text direction. For English that is horizontal. `block` means perpendicular to the text direction. For English that is vertical.

## Mapping

| Physical | Logical |
|----------|---------|
| `margin-left` | `margin-inline-start` |
| `margin-right` | `margin-inline-end` |
| `padding-top` | `padding-block-start` |
| `padding-bottom` | `padding-block-end` |
| `width` | `inline-size` |
| `height` | `block-size` |

```css
.container {
  inline-size: min(100% - 2rem, 70rem);
  margin-inline: auto;
}
```

`margin-inline: auto` centres a block regardless of writing direction.

## When to use logical properties

- Use them for spacing that should follow the text flow.
- Use them when a page may be translated or displayed in a different writing mode.
- For simple English-only pages, physical properties still work. `margin-inline: auto` is a good habit to start with.

```css
.card {
  padding-inline: 1rem;
  padding-block: 0.75rem;
  border-inline-start: 3px solid #0a58ca;
}
```

## Try it

1. Take a card with `padding-left`, `padding-right`, `margin-top`, and `margin-bottom`.
2. Rewrite the properties using logical equivalents.
3. Centre a container with `margin-inline: auto`.
4. Add a thick border on the start side with `border-inline-start`.
5. Check the page in the browser. It should look the same for English text.

If a logical property seems to do nothing, check the browser's support and whether the element has a writing mode override.

Next: [Custom Properties](14-custom-properties.md)
