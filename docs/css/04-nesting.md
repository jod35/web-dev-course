# Nesting

Nesting lets you write a selector inside another, so related rules stay together. It mirrors how your HTML is nested.

## Without nesting

```css
.card { padding: 1rem; border: 1px solid #ddd; }
.card h2 { margin: 0 0 0.5rem 0; }
.card p { color: #444; }
.card a { text-decoration: none; }
```

## With nesting

```css
.card {
  padding: 1rem;
  border: 1px solid #ddd;

  h2 { margin: 0 0 0.5rem 0; }
  p { color: #444; }
  a { text-decoration: none; }
}
```

Both do the same thing. Nesting just keeps the `.card` family together.

## The `&` — refer to the parent

`&` means “the current selector.” Use it for states and modifiers:

```css
.btn {
  padding: 0.5rem 1rem;
  background: #eee;

  &:hover { background: #ddd; }
  &:focus-visible { outline: 2px solid #333; }

  &.primary {
    background: #0a58ca;
    color: #fff;
  }
}
```

Compiles to `.btn:hover`, `.btn:focus-visible`, `.btn.primary`.

## When to nest

- Group a component and its children: `.card { h2, p, a { ... } }`
- Add states: `&:hover`, `&:focus`
- Nest media queries:

```css
.card {
  padding: 1rem;

  @media (min-width: 640px) {
    padding: 1.5rem;
  }
}
```

## When not to nest

Do not nest deeply just because you can:

```css
/* too deep, hard to override */
.page .content .card .header h2 a { color: crimson; }
```

Prefer a class on the target:

```css
.card-title { color: crimson; }
```

And inside:

```css
.card {
  .card-title { color: crimson; }
}
```

One level, maybe two, is enough. If you need three, add a class.

## Recap

| Use | Example |
|-----|---------|
| Group children | `.card { h2 { ... } }` |
| States | `&:hover`, `&:focus-visible` |
| Modifier | `&.primary` |
| Keep it shallow | One level is ideal |

Nesting is convenience, not a requirement. Your CSS works the same with or without it.
