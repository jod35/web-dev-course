# 19 - Mini Project: Bakery Page

**Goal:** prove Chapters 01–18 by building one complete page from a spec.

## Spec,build `bakery.html`

1. Full boilerplate: `<!DOCTYPE>`, `<html lang="en">`, `<head>` with `charset`, `viewport`, `<title>Bakery</title>`.
2. `<body>` containing, in order:
    - `<header>` with `<h1>` page title (exactly one) + `<nav>` menu list linking to `#menu` and `#prices`.
    - `<main>` (exactly one) holding:
    - `<p>` intro with one `<strong>` and one `<em>`.
    - `<section>` "Our Menu": `<h2>` + `<ul>` of 3 items; one item with a nested `<ul>` of 2.
    - `<hr>` between Menu and Prices.
    - `<section>` "Prices": `<h2 id="prices">` + table with `<caption>`, `<thead>` (`th scope="col"` ×2), two `<tbody>` rows.
    - `<div class="card">` grouping one menu item or price note (generic box, no heading of its own).
    - `<blockquote>` with `cite` URL + `<cite>` source.
    - `<img>` with meaningful `alt` (any `src` filename).
    - Internal link `<a href="#prices">` jumping to `<h2 id="prices">`.
    - Order `<form method="post">` with labeled `text` + `number` inputs and a submit `<button>`.
    - `<footer>` with `<address>` contact and `<small>` copyright.

## Checklist (self-grade)

- [ ] Boilerplate order: doctype → html → head → body, closes reversed.
- [ ] Landmarks: one `<header>` + `<nav>`, exactly one top-level `<main>`, one `<footer>`.
- [ ] Menu and Prices each wrapped in `<section>` with their own `<h2>`; no heading-free `<section>`.
- [ ] One `<h1>`, no skipped heading levels.
- [ ] Every `<img>` has `alt`; every input has `<label>` + `name`.
- [ ] No `<br>` stacking, no table-for-layout, no `<div id="header">`-style fake landmarks, link text describes destinations.
- [ ] Open in a browser: headings sized by level, table grid readable, form blocks empty submit (`required`).

## Stretch goals

- Add `<time datetime>` opening hours and `<del>`/`<ins>` price update.
- Add `<figure>`/`<figcaption>` around the image.
- Validate at `validator.w3.org`,fix every error.

**Prev:** [18,Page Landmarks](18-landmarks.md) · **Index:** [00,Index](00-index.md)
