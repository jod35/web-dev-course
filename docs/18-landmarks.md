# 18 - Page Landmarks: header, nav, main, footer, article, aside

**Goal:** In this chapter you will build a complete page skeleton with landmark tags which screen readers and search engines understand.

## Why not only `div`?

Chapter 17 introduced generic boxes. The following page uses only those boxes:

```html
<div id="header">
  <div class="nav">…</div>
</div>
<div id="main">…</div>
<div id="footer">…</div>
```

It renders correctly, but assistive technology sees three identical boxes. Landmark tags state **what each box is**:

```html
<header>…</header>
<nav>…</nav>
<main>…</main>
<footer>…</footer>
```

Screen-reader users can jump straight to the `<nav>` or `<main>` element, while search engines weigh the `<main>` content most heavily.

## Tag reference

### `<header>` - intro of page or section

The `header` element holds the banner of a page, such as the logo and title, or the intro of a `section` or `article` element. It is not limited to one per page, because it applies once per scope:

```html
<header>
  <h1>Bakery</h1>
  <p>Fresh bread daily.</p>
</header>
```

### `<nav>` - major navigation

The `nav` element wraps the main menu, which is almost always a list in the Chapter 14 pattern:

```html
<nav>
  <ul>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#prices">Prices</a></li>
  </ul>
</nav>
```

Use the `nav` element only for major navigation such as the site menu or table of contents, not for every group of links.

### `<main>` - the page's core

The `main` element holds the unique central content of the page. Two rules apply: each page contains **exactly one** `main` element, and it must never sit inside `header`, `footer`, or `nav`:

```html
<main>
  <section>
    <h2>Our Menu</h2>
    <p>…</p>
  </section>
</main>
```

### `<footer>` - closing of page or section

The `footer` element holds author information, copyright, and contact details, and it pairs naturally with `<address>` and `<small>` from Chapter 11:

```html
<footer>
  <address>hello@mhsm.web</address>
  <small>© 2026 MHSM. All rights reserved.</small>
</footer>
```

### `<article>` vs `<section>` vs `<aside>`

| Tag | Question it answers | Example |
|-----|---------------------|---------|
| `article` | Could this piece stand alone if it were syndicated or shared? | A recipe or a news post |
| `section` | Is this a themed part of something larger? | The "Our Menu" section inside the bakery page |
| `aside` | Is this tangential content such as a sidebar, tip, or ad? | An opening-hours box beside the menu |

```html
<main>
  <article>
    <h2>Sourdough Recipe</h2>
    <p>Mix flour and water…</p>
  </article>
  <aside>
    <h2>Tip</h2>
    <p>Best eaten warm.</p>
  </aside>
</main>
```

A recipe in an `article` element could be reposted on its own. A tip in an `aside` element only makes sense beside the main content.

## Full skeleton

Chapters 01, 17, and 18 combine into the following structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Bakery</title>
</head>
<body>
  <header>
    <h1>Bakery</h1>
    <nav>
      <ul>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#prices">Prices</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>
      <h2 id="menu">Our Menu</h2>
      <div class="card">
        <h3>Bread</h3>
        <p>Fresh daily.</p>
      </div>
    </section>
    <section>
      <h2 id="prices">Prices</h2>
      <p>Updated weekly.</p>
    </section>
  </main>
  <footer>
    <address>hello@mhsm.web</address>
    <small>© 2026 MHSM. All rights reserved.</small>
  </footer>
</body>
</html>
```

## Rules

- Use one `<main>` element per page. Extra `main` elements confuse navigation, because readers cannot tell which block is the real content.
- Do not place `<main>` inside `<header>`, `<footer>`, or `<nav>`, because it must form a top-level zone of `<body>`.
- When `header` or `footer` sits inside an `article` or `section` element, it belongs to that block rather than to the whole page.
- Do not fake landmarks with `<div id="header">`, because the rendering is the same but the meaning is lost.

## Recap

| Tag | Job | Rule |
|-----|-----|------|
| `header` | Intro or banner | One per page or per section and article |
| `nav` | Major navigation | Wraps a list, not every link |
| `main` | Core content | Exactly one per page, at the top level of `body` |
| `footer` | Closing and contact | Pairs with `address` and `small` |
| `article` | Standalone piece | Must make sense on its own |
| `aside` | Tangential box | Sidebar, tip, or related links |
