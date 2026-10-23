# Practice: Build a Page

This chapter puts the HTML and CSS tracks together. You will build one complete page with a header, navigation, content cards, and a footer.

Create a folder with two files: `index.html` and `styles.css`.

## `index.html`

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>MHSM Bakery</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <h1>MHSM Bakery</h1>
    <p>Fresh bread baked every morning.</p>
  </header>

  <nav class="navbar">
    <a href="#">Home</a>
    <a href="#">Menu</a>
    <a href="#">Contact</a>
  </nav>

  <main class="container">
    <h2>Today's bread</h2>

    <section class="cards">
      <article class="card">
        <h3>White bread</h3>
        <p>Soft and fresh, baked at 6am.</p>
      </article>

      <article class="card">
        <h3>Brown bread</h3>
        <p>Hearty and wholesome.</p>
      </article>

      <article class="card">
        <h3>Tea buns</h3>
        <p>Perfect with morning tea.</p>
      </article>
    </section>
  </main>

  <footer class="site-footer">
    <small>&copy; 2026 MHSM. All rights reserved.</small>
  </footer>
</body>
</html>
```

Notice the heading order: one `<h1>`, one `<h2>` for the section, and `<h3>` for each card. The links use `#` because this is a single practice page.

## `styles.css`

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
  color: #222;
}

.site-header,
.site-footer,
.navbar {
  padding: 1rem;
}

.site-header {
  background: #111;
  color: #fff;
}

.site-header p {
  margin: 0;
  color: #ddd;
}

.navbar {
  display: flex;
  gap: 1rem;
  border-bottom: 1px solid #eee;
}

.navbar a {
  color: #0a58ca;
  text-decoration: none;
}

.navbar a:hover {
  text-decoration: underline;
}

.navbar a:focus-visible {
  outline: 2px solid #333;
  outline-offset: 2px;
}

.container {
  width: min(100% - 2rem, 70rem);
  margin-inline: auto;
  padding-block: 1.5rem;
}

.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
}

.card {
  padding: 1rem;
  border: 1px solid #ddd;
  border-radius: 0.5rem;
}

.card h3 {
  margin-top: 0;
}

.site-footer {
  border-top: 1px solid #eee;
  text-align: center;
  color: #666;
}
```

## Check your work

Open `index.html` in the browser and confirm:

- The stylesheet is linked and the page has the dark header.
- The navigation sits in one row on a wide screen.
- The cards sit in a grid and stack on a narrow screen.
- The page has one `<h1>`, one `<h2>`, and three `<h3>` elements.
- The footer copyright is visible.
- Tab through the links. The focus outline is visible.

If the page has no styles, check the `href` in the `<link>` element. If the cards overflow, check the `minmax()` value and the container width.

## What to try next

- Change `repeat(auto-fit, minmax(220px, 1fr))` to `repeat(3, 1fr)` and reload at a narrow width. Note what breaks, then restore the original.
- Change the navbar from `gap` to `justify-content: space-between`.
- Add a fourth card and check that the grid still fits.
- Replace the hex colours with `hsl()` values.
- Add a `max-width: 65ch` to the card paragraphs and compare the line length.
- Add a media query that reduces the header padding below `640px`.

## Where to go next

- Rebuild one of your HTML course pages with this stylesheet.
- Add a second page and a shared stylesheet.
- Practise reading the browser's inspector until you can tell which rule is winning.
- When the JavaScript track is available, use it to add behaviour to a page like this one.

You have now used selectors, the box model, colour, typography, flexbox, grid, spacing, and responsive media queries in one page. That covers most of the CSS you will use day to day.
