# 18 - Page Landmarks: header, nav, main, footer, article, aside

**Goal:** build a full page skeleton with landmark tags screen readers and search engines understand.

## Why not only `div`?

Chapter 17 gave you generic boxes. This page uses only them:

```html
<div id="header">
  <div class="nav">…</div>
</div>
<div id="main">…</div>
<div id="footer">…</div>
```

It renders fine, but assistive tech sees three identical boxes. Landmark tags say **what each box is**:

```html
<header>…</header>
<nav>…</nav>
<main>…</main>
<footer>…</footer>
```

Screen-reader users jump straight to `<nav>` or `<main>`; search engines weigh `<main>` content highest.

## Tag reference

### `<header>`,intro of page or section

Page banner (logo, title) or the intro of a `section`/`article`. Not one-per-page,one per scope:

```html
<header>
  <h1>Bakery</h1>
  <p>Fresh bread daily.</p>
</header>
```

### `<nav>`,major navigation

Wraps the main menu,almost always a list (Chapter 14 pattern):

```html
<nav>
  <ul>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#prices">Prices</a></li>
  </ul>
</nav>
```

Use `nav` only for major navigation (site menu, table of contents),not every link group.

### `<main>`,the page's core

The unique central content. Rules: **exactly one** per page, never nested inside `header`/`footer`/`nav`:

```html
<main>
  <section>
    <h2>Our Menu</h2>
    <p>…</p>
  </section>
</main>
```

### `<footer>`,closing of page or section

Author info, copyright, contact (pairs with `<address>` and `<small>` from Chapter 11):

```html
<footer>
  <address>hello@mhsm.web</address>
  <small>© 2026 MHSM. All rights reserved.</small>
</footer>
```

### `<article>` vs `<section>` vs `<aside>`

| Tag | Question it answers | Example |
|-----|---------------------|---------|
| `article` | Could this stand alone (syndicated, shared)? | A recipe, a news post |
| `section` | Is this a themed part of something bigger? | "Our Menu" inside the bakery page |
| `aside` | Is this tangential (sidebar, tip, ad)? | Opening-hours box beside the menu |

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

A recipe (`article`) could be reposted on its own. The tip (`aside`) only makes sense beside it.

## Full skeleton

Chapters 01 + 17 + 18 together:

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

```text
<body>             all visible content
  <header>         banner + <nav>
  <main>           ONE core,holds <section>s
    <section>      themed group,has <h2>
      <div>        generic box,styled via class
  <footer>         contact + fine print
```

## Gotchas

- One `<main>` per page. Extra mains confuse navigation ("which one is the content?").
- Don't put `<main>` inside `<header>`, `<footer>`, or `<nav>`,it must be a top-level zone of `<body>`.
- `header`/`footer` inside an `article`/`section` belong to that block,not the whole page.
- Don't fake landmarks with `<div id="header">`,same rendering, zero meaning.

## Recap

| Tag | Job | Rule |
|-----|-----|------|
| `header` | Intro/banner | Per page or per section/article |
| `nav` | Major navigation | Wraps a list, not every link |
| `main` | Core content | Exactly one, top-level in `body` |
| `footer` | Closing/contact | Pairs with `address` + `small` |
| `article` | Standalone piece | Must make sense on its own |
| `aside` | Tangential box | Sidebar, tip, related links |

**Next:** [19,Mini Project](19-mini-project.md) · **Prev:** [17,Grouping](17-div-section.md)
