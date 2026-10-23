# Flexbox

Flexbox is for one-dimensional layout: a row or a column where you want to align and distribute items.

## A basic row

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
  flex: 1;
  padding: 1rem;
  border: 1px solid #ddd;
}
```

`gap` adds space between items without margin tricks. `flex: 1` makes each card share the available space equally.

## Direction and wrapping

```css
.row {
  display: flex;
  flex-direction: row; /* default */
}

.col {
  display: flex;
  flex-direction: column;
}

.wrap {
  display: flex;
  flex-wrap: wrap;
}
```

`wrap` lets items move to the next line when there is not enough room. This can replace a media query for simple card rows.

## Alignment

Flexbox has a main axis and a cross axis. For a row, the main axis is horizontal and the cross axis is vertical.

```css
.row {
  display: flex;
  justify-content: space-between; /* main axis */
  align-items: center;            /* cross axis */
}
```

Common values:

- `justify-content`: `flex-start`, `center`, `flex-end`, `space-between`, `space-around`, `space-evenly`.
- `align-items`: `stretch`, `center`, `flex-start`, `flex-end`.

## A navigation bar

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

.navbar nav {
  display: flex;
  gap: 1rem;
}
```

The outer flex row separates the name from the links. The inner flex row spaces the links.

## Flexbox or Grid?

- **Flexbox:** a row or column of items, navigation, button groups, centering a single item.
- **Grid:** a two-dimensional layout with rows and columns, such as a page skeleton or card grid.

If you only need to distribute items in one direction, start with flexbox.

## Try it

1. Build a navigation bar with a title on the left and three links on the right.
2. Make a row of three cards with `gap` and `flex: 1`.
3. Change `justify-content` to `center` and then `space-between`. Which one suits the navigation?
4. Add `flex-wrap: wrap` and make the window narrow.
5. Add a fourth card and check that all cards still share the space evenly.

If the items are squashed, check whether they have a minimum width or whether the container is wrapping.

Next: [Grid](12-grid.md)
