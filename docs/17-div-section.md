# 17 - Grouping: div, section, span

**Goal:** In this chapter you will learn how to group content with `div` for generic blocks, `section` for thematic blocks, and `span` for inline runs.

## The problem

So far every tag has described one thing, such as a heading, a paragraph, or a list item. Real pages also need **containers**, which are boxes that hold several tags together so that you can move, style, or name them as a unit:

```html
<h2>Our Menu</h2>
<ul>
  <li>Bread</li>
  <li>Milk</li>
</ul>
<h2>Prices</h2>
<table>…</table>
```

Which parts belong together? Without containers, CSS and screen readers see one flat list. The `div` and `section` elements solve that problem.

## Tag reference

### `<div>` - generic block container

The `div` element is a block-level box with **no meaning**. It groups things together for styling or scripting:

```html
<div class="card">
  <h2>Bread</h2>
  <p>Fresh daily.</p>
</div>
```

- The `class` attribute names the group for CSS, so the value `"card"` can repeat on many boxes.
- The `id` attribute names one unique box on the page, so the value `id="prices"` can appear only once, and links can jump to it with `<a href="#prices">`.

```html
<div id="prices">
  <h2>Prices</h2>
  <p>Updated weekly.</p>
</div>
```

### `<section>` - thematic group

A `section` is a `div` **with meaning**, because it marks a themed chunk of the page in the same way a chapter marks a book. The rule is that **every `<section>` element needs a heading** from `h1` to `h6` as its first child:

```html
<section>
  <h2>Our Menu</h2>
  <ul>
    <li>Bread</li>
    <li>Milk</li>
  </ul>
</section>
```

If the group has no heading, use a `<div>` element instead of a `<section>` element:

```html
<!-- Wrong: section with no heading -->
<section>
  <p>Just a styled box.</p>
</section>

<!-- Right: generic box -->
<div class="notice">
  <p>Just a styled box.</p>
</div>
```

### `<span>` - inline div

The `span` element is the inline counterpart of `div`. It is a meaning-free wrapper which sits inside a sentence:

```html
<p>Result: <span class="price">$1</span></p>
```

| Container | Block or inline? | Meaning? | Rule |
|-----------|------------------|----------|------|
| `div` | Block | None | Group for styling or scripting |
| `section` | Block | Thematic group | Must contain a heading |
| `span` | Inline | None | Never wrap whole paragraphs |

### Decision rule

```text
Need a wrapper?
  ├─ Themed chunk with a heading? → <section>
  ├─ Inside a sentence/word?      → <span>
  └─ Otherwise (styling hook)?    → <div>
```

## Nesting

Containers nest in the same way as all HTML elements, so the inner element closes before the outer element:

```html
<section>
  <h2>Our Menu</h2>
  <div class="card">
    <h3>Bread</h3>
    <p>Price: <span class="price">$1</span></p>
  </div>
</section>
```

```text
<section>          thematic group
  <h2>             its heading,required
  <div>            generic box inside
    <h3> + <p>    visible content
    <span>         inline hook inside <p>
```

## Rules

- Do not use `div` where a precise tag fits. A list of items is a `<ul>` element rather than a set of `<div>` elements, and tabular data is a `<table>` element rather than a set of `<div>` elements.
- Do not wrap every single element in a `div` element. Group things which belong together, because extra boxes add noise for readers and for CSS.
- The `id` values must be unique on each page, while `class` values may repeat.
- A `<div>` element cannot go inside a `<p>` element, because the browser closes the paragraph early. A `<span>` element can sit inside a paragraph.

## Recap

| Tag | Job | Watch out |
|-----|-----|-----------|
| `div` | Generic block group | It has no meaning, so it needs `class` or `id` to be useful |
| `section` | Themed group | It must have a heading, otherwise use `div` |
| `span` | Generic inline group | It belongs inside sentences only |

**Next:** [18 - Page Landmarks](18-landmarks.md) · **Prev:** [16 - Forms Basics](16-forms-basics.md)
