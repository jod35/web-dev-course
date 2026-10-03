# Grid

Grid is for **two-dimensional layout**: rows *and* columns together, exactly what you need for page skeletons.

## A simple page grid

```html
<div class="layout">
  <header>Header</header>
  <nav>Navigation</nav>
  <main>Main content</main>
  <aside>Aside</aside>
  <footer>Footer</footer>
</div>
```

```css
.layout {
  display: grid;
  grid-template-columns: 200px 1fr;
  grid-template-areas:
    "header header"
    "nav    main"
    "nav    aside"
    "footer footer";
  gap: 1rem;
}
header { grid-area: header; }
nav    { grid-area: nav; }
main   { grid-area: main; }
aside  { grid-area: aside; }
footer { grid-area: footer; }
```

`1fr` means one fraction of remaining space. `200px 1fr` gives a fixed sidebar and flexible main column.

## Without named areas

You can also place by line numbers:

```css
.layout {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 1rem;
}
header { grid-column: 1 / -1; } /* span all columns */
```

`1 / -1` means from first line to last line, handy for full-width headers and footers.

## Responsive grid — no media query

For cards that auto-fit:

```css
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
}
```

As the viewport shrinks, cards wrap automatically. This one line replaces a lot of flex wrapping logic.

## Grid vs flexbox

- **Grid** — page layout, two axes, explicit rows and columns.
- **Flexbox** — content distribution in one axis, navigation, button groups.

Many pages use both: grid for the outer layout, flex inside cards or navs.

```css
.page { display: grid; grid-template-columns: 240px 1fr; gap: 1rem; }
.navbar { display: flex; justify-content: space-between; }
```

## Recap

| Property | Role |
|----------|------|
| `display: grid` | Grid container |
| `grid-template-columns` | Column sizes (`200px 1fr`, `repeat(...)`) |
| `grid-template-areas` | Named layout map |
| `gap` | Gutters |
