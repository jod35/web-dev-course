# Lists

Lists are how we structure related items — shopping, steps, terms and definitions — without losing the relationship between them.

## `<ul>` — unordered list

`ul` is a bulleted list where **order doesn't matter**. Each item is an `<li>`:

```html
<ul>
  <li>Bread</li>
  <li>Milk</li>
  <li>Eggs</li>
</ul>
```

## `<ol>` — ordered list

`ol` is a numbered list where **order matters** — steps, rankings. The browser numbers them for you:

```html
<ol>
  <li>Mix flour and water.</li>
  <li>Knead ten minutes.</li>
  <li>Bake at 220°C.</li>
</ol>
```

Need to start elsewhere or count backwards? Use `start` or `reversed`:

```html
<ol start="5">
  <li>Fifth step first</li>
</ol>
```

## Nesting lists

An `<li>` can hold an entire sub-list — and the nested list belongs **inside** that `<li>`, not after it:

```html
<ul>
  <li>Bread
    <ul>
      <li>White</li>
      <li>Brown</li>
    </ul>
  </li>
  <li>Milk</li>
</ul>
```

That's the pattern you'll see for menus and grouped items.

## `<dl>` — description list

`dl` handles term + definition pairs — glossaries, menus with descriptions, metadata:

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language — page structure.</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets — page styling.</dd>
</dl>
```

| Tag | Role |
|-----|------|
| `dl` | The whole description list |
| `dt` | Term |
| `dd` | Definition or description |

## A few habits to keep

- Only `<li>` may sit directly inside `ul` or `ol` — no bare text or `<p>` wrappers at that level.
- Don't fake a list with `<br>` or `-` dashes. You'll lose count, semantics and accessibility in one go.
- Navigation menus are just lists — you'll see `<nav><ul>…` everywhere, so get comfortable with it.

## Recap

| List | When to use it | Markers |
|------|----------------|---------|
| `ul` | Order doesn't matter | Bullets |
| `ol` | Order matters | Numbers, added automatically |
| `dl` | Term → definition | None |
