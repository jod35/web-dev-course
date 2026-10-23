# Lists

Lists group related items and keep the relationship between them clear. HTML has three main list types.

## Unordered lists: `<ul>`

Use `<ul>` when the order of the items does not matter:

```html
<ul>
  <li>Bread</li>
  <li>Milk</li>
  <li>Eggs</li>
</ul>
```

Browsers show each item with a bullet. Every item goes inside `<li>`.

## Ordered lists: `<ol>`

Use `<ol>` when the order matters:

```html
<ol>
  <li>Mix the flour and water.</li>
  <li>Knead the dough for ten minutes.</li>
  <li>Bake at 220°C.</li>
</ol>
```

Browsers number the items automatically. You can change the starting number:

```html
<ol start="5">
  <li>Fifth step</li>
  <li>Sixth step</li>
</ol>
```

## Nested lists

A nested list goes inside an `<li>`, not after it:

```html
<ul>
  <li>
    Bread
    <ul>
      <li>White</li>
      <li>Brown</li>
    </ul>
  </li>
  <li>Milk</li>
</ul>
```

This creates a sub-list under "Bread". The outer list still has two items.

## Description lists: `<dl>`

Use `<dl>` for term and definition pairs:

```html
<dl>
  <dt>HTML</dt>
  <dd>The structure and meaning of a page.</dd>

  <dt>CSS</dt>
  <dd>The presentation of a page.</dd>
</dl>
```

- `<dl>` is the list.
- `<dt>` is the term.
- `<dd>` is the definition.

Description lists are useful for glossaries, menus with descriptions, and metadata.

## Rules for list markup

- Only `<li>` may be a direct child of `<ul>` or `<ol>`.
- Keep the entire nested list inside the `<li>` it belongs to.
- Do not fake a list with dashes or `<br>`. You lose the structure and screen readers cannot announce the number of items.
- Navigation menus are often lists. You will see `<nav><ul>...</ul></nav>` in real pages.

## Exercise: build a shop list

Create a page with:

1. An unordered list of three bread types.
2. A nested list under one bread type showing two sizes.
3. An ordered list of four steps for making tea.
4. A description list with two terms and their definitions.

Check that each nested list is inside an `<li>` and that every item uses `<li>`. Then use the browser's accessibility inspector, if available, to confirm the list is announced as a list.

Next: [Tables](15-tables.md)
