# Grid

Grid is for two-dimensional layout: rows and columns together. It is a good fit for page skeletons and card collections.

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

`1fr` means one fraction of the remaining space. `200px 1fr` gives a fixed sidebar and a flexible main column.

## Placing items by line

You can also place items without named areas:

```css
.layout {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 1rem;
}

header {
  grid-column: 1 / -1;
}
```

`1 / -1` means from the first column line to the last one. It is useful for a full-width header or footer.

## Responsive cards without a media query

```css
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
}
```

`auto-fit` creates as many columns as fit. `minmax(220px, 1fr)` keeps each column at least `220px` wide, then lets it grow. On a narrow screen, the cards stack without a separate media query.

## Grid or Flexbox?

- **Grid:** page layout, two dimensions, explicit rows and columns.
- **Flexbox:** distribution in one direction, navigation, button groups.

Many pages use both: grid for the outer layout and flexbox inside cards or navigation.

```css
.page {
  display: grid;
  grid-template-columns: 240px 1fr;
  gap: 1rem;
}

.navbar {
  display: flex;
  justify-content: space-between;
}
```

## Try it

1. Build the page grid from the first example.
2. Change the sidebar from `200px` to `minmax(160px, 240px)` and see how it adapts.
3. Add a card collection using `repeat(auto-fit, minmax(220px, 1fr))`.
4. Make the window narrow and check that the cards wrap.
5. Replace the named areas with line-based placement. Which version is easier to read?

If a grid item lands in the wrong place, check the number of columns and the order of the `grid-area` names.

Next: [Logical Properties](13-logical-properties.md)
