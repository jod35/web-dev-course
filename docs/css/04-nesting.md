# Nesting

CSS nesting lets you write a selector inside another rule. It keeps related styles together and mirrors the structure of your HTML.

Native CSS nesting is supported in current browsers. If you need to support an older browser, write the selectors separately.

## Without nesting

```css
.card {
  padding: 1rem;
  border: 1px solid #ddd;
}

.card h2 {
  margin: 0 0 0.5rem;
}

.card p {
  color: #444;
}

.card a {
  text-decoration: none;
}
```

## With nesting

```css
.card {
  padding: 1rem;
  border: 1px solid #ddd;

  h2 {
    margin: 0 0 0.5rem;
  }

  p {
    color: #444;
  }

  a {
    text-decoration: none;
  }
}
```

Both versions do the same thing. The nested version keeps the `.card` styles in one place.

## The `&` selector

`&` refers to the parent selector. Use it for states and modifiers:

```css
.btn {
  padding: 0.5rem 1rem;
  background: #eee;

  &:hover {
    background: #ddd;
  }

  &:focus-visible {
    outline: 2px solid #333;
    outline-offset: 2px;
  }

  &.primary {
    background: #0a58ca;
    color: #fff;
  }
}
```

This compiles to `.btn:hover`, `.btn:focus-visible`, and `.btn.primary`.

## Nesting media queries

Media queries can also be nested:

```css
.card {
  padding: 1rem;

  @media (min-width: 640px) {
    padding: 1.5rem;
  }
}
```

This keeps the responsive change next to the component it affects.

## When not to nest

Do not nest just because you can. Deep selectors are hard to override:

```css
/* avoid */
.page .content .card .header h2 a {
  color: crimson;
}
```

Prefer a class on the target:

```css
.card-title {
  color: crimson;
}
```

One level of nesting is usually enough. If you need three, add a class instead.

## Try it

Take a card component and write its styles without nesting. Then rewrite them with nesting.

1. Put the card's own properties in the outer rule.
2. Nest the `h2`, `p`, and `a` rules inside `.card`.
3. Add `&:hover` and `&:focus-visible` states.
4. Add a nested media query that changes the padding at `640px`.

Open the page and check that the styles still apply. If they do not, confirm that the opening and closing braces match.

Next: [The Cascade](05-cascade.md)
