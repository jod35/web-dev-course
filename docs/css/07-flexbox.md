# Flexbox

Flexbox is for **one-dimensional layout**: a row or a column where you want to align and distribute items.

## Basic row

```html
<div class="row">
  <div class="card">A</div>
  <div class="card">B</div>
  <div class="card">C</div>
</div>
```

```css
.row {
  display: flex;
  gap: 1rem;
}
.card {
  flex: 1; /* share space equally */
  padding: 1rem;
  border: 1px solid #ddd;
}
```

`gap` adds space between flex items without margin tricks.

## Direction and wrapping

```css
.row { display: flex; flex-direction: row; } /* default */
.col { display: flex; flex-direction: column; }
.wrap { display: flex; flex-wrap: wrap; }
```

`wrap` lets items flow to the next line on small screens, no media query needed.

## Alignment

Two axes to remember:

```css
.row {
  display: flex;
  justify-content: space-between; /* main axis (horizontal for row) */
  align-items: center;             /* cross axis (vertical for row) */
}
```

Try: `justify-content: flex-start | center | space-between | space-around` and `align-items: stretch | center | flex-start | flex-end`.

## A common pattern — navbar

```html
<header class="navbar">
  <strong>MHSM</strong>
  <nav>
    <a href="#">Home</a>
    <a href="#">Courses</a>
    <a href="#">Contact</a>
  </nav>
</header>
```

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.75rem 1rem;
  border-bottom: 1px solid #eee;
}
.navbar nav { display: flex; gap: 1rem; }
```

## When to use flex vs grid

- **Flexbox** — a line of items, navigation, card rows, centering a button.
- **Grid** — a two-dimensional page layout, next chapter.

If you only need to distribute items in one direction, reach for flex first.

## Recap

| Property | What it controls |
|----------|------------------|
| `display: flex` | Turns container into flex |
| `gap` | Space between items |
| `justify-content` | Main-axis distribution |
| `align-items` | Cross-axis alignment |
| `flex: 1` | Grow to fill available space |
