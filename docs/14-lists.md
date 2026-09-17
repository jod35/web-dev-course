# 14,Lists

**Goal:** structure related items with unordered, ordered, and description lists.

## `<ul>`,unordered list

Bulleted items, order doesn't matter. Each item is an `<li>`:

```html
<ul>
  <li>Bread</li>
  <li>Milk</li>
  <li>Eggs</li>
</ul>
```

## `<ol>`,ordered list

Numbered items, order matters,steps, rankings. Browsers number automatically:

```html
<ol>
  <li>Mix flour and water.</li>
  <li>Knead ten minutes.</li>
  <li>Bake at 220°C.</li>
</ol>
```

Start numbering elsewhere with `start`, reverse with `reversed`:

```html
<ol start="5">
  <li>Fifth step first</li>
</ol>
```

## Nesting lists

An `<li>` can hold a whole sub-list,the nested list goes **inside** the `<li>`, not after it:

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

## `<dl>`,description list

Term/definition pairs,glossaries, menus with descriptions, metadata:

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language,page structure.</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets,page styling.</dd>
</dl>
```

| Tag | Job |
|-----|-----|
| `dl` | The whole description list |
| `dt` | Term |
| `dd` | Definition/description |

## Gotchas

- Only `<li>` may be a direct child of `ul`/`ol`,no bare text or `<p>` wrappers at that level.
- Don't fake lists with `<br>` or `-` dashes; readers lose the count and structure.
- Navigation menus are lists too (`<nav><ul>…`),you'll meet this pattern constantly.

## Recap

| List | Use when | Markers |
|------|----------|---------|
| `ul` | Order irrelevant | Bullets |
| `ol` | Order matters | Numbers (auto) |
| `dl` | Term → definition | None |

**Next:** [15,Tables](15-tables.md) · **Prev:** [13,Images](13-images.md)
