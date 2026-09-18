# 14 - Lists

**Goal:** In this chapter you will learn how to structure related items with unordered, ordered, and description lists.

## `<ul>` - unordered list

The `ul` element defines a bulleted list in which the order of the items does not matter. Each item is an `<li>` element:

```html
<ul>
  <li>Bread</li>
  <li>Milk</li>
  <li>Eggs</li>
</ul>
```

## `<ol>` - ordered list

The `ol` element defines a numbered list in which the order matters, for example for steps or rankings. Browsers number the items automatically:

```html
<ol>
  <li>Mix flour and water.</li>
  <li>Knead ten minutes.</li>
  <li>Bake at 220°C.</li>
</ol>
```

Start the numbering elsewhere with the `start` attribute, or reverse it with the `reversed` attribute:

```html
<ol start="5">
  <li>Fifth step first</li>
</ol>
```

## Nesting lists

An `<li>` element can hold a complete sub-list. The nested list goes **inside** the `<li>` element, not after it:

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

## `<dl>` - description list

The `dl` element defines term and definition pairs, which are useful for glossaries, menus with descriptions, and metadata:

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
| `dd` | Definition or description |

## Rules

- Only an `<li>` element may be a direct child of `ul` or `ol`, so do not place bare text or `<p>` wrappers at that level.
- Do not fake lists with `<br>` tags or `-` dashes, because readers then lose the count and the structure.
- Navigation menus are lists too, and you will meet the `<nav><ul>…` pattern constantly.

## Recap

| List | Use when | Markers |
|------|----------|---------|
| `ul` | Order is irrelevant | Bullets |
| `ol` | Order matters | Numbers, added automatically |
| `dl` | Term leads to definition | None |

**Next:** [15 - Tables](15-tables.md) · **Prev:** [13 - Images](13-images.md)
