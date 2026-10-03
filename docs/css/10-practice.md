# Putting It Together

Lets build a tiny, complete page that uses both tracks: HTML for structure, CSS for presentation. Copy these two files into one folder and open `index.html`.

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
    <p class="lead">Fresh bread baked every morning</p>
  </header>

  <nav class="navbar">
    <a href="#">Home</a>
    <a href="#">Menu</a>
    <a href="#">Contact</a>
  </nav>

  <main class="container">
    <section class="cards">
      <article class="card">
        <h2>White Bread</h2>
        <p>Soft and fresh, baked at 6am.</p>
      </article>
      <article class="card">
        <h2>Brown Bread</h2>
        <p>Hearty and wholesome.</p>
      </article>
      <article class="card">
        <h2>Tea Buns</h2>
        <p>Perfect with morning tea.</p>
      </article>
    </section>
  </main>

  <footer class="site-footer">
    <small>© 2026 MHSM. All rights reserved.</small>
  </footer>
</body>
</html>
```

## `styles.css`

```css
* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
  color: #222;
}

.site-header, .site-footer, .navbar {
  padding: 1rem;
}

.site-header {
  background: #111;
  color: #fff;
}
.lead { color: #ccc; margin: 0; }

.navbar {
  display: flex;
  gap: 1rem;
  border-bottom: 1px solid #eee;
}
.navbar a { text-decoration: none; color: #0a58ca; }
.navbar a:hover { text-decoration: underline; }

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

.site-footer {
  border-top: 1px solid #eee;
  text-align: center;
  color: #666;
}
```

## What to try next

- Change `repeat(auto-fit, minmax(220px, 1fr))` to `repeat(3, 1fr)` and watch what breaks on narrow screens.
- Swap the navbar flex for `justify-content: space-between`.
- Add a media query that hides the `.lead` paragraph below `640px`.
- Replace hex colors with `hsl` and make the header slightly lighter.

You have now used selectors, box model, colors, type, flex/grid, and responsive habits together. That is most of day-to-day CSS.

## Where to go after

- Rebuild one of your HTML course pages with this CSS structure.
- Add a new CSS file per section and practice linking multiple stylesheets while keeping specificity low.
- When you are ready, the JavaScript track will add behavior on top of this structure and style.

Great work reaching the end of the CSS track.
