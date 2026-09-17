# 17 - Grouping: div, section, span

**Goal:** group content with `div` (generic), `section` (thematic), and `span` (inline).

## The problem

So far every tag describes one thing: a heading, a paragraph, a list item. Real pages need **containers**,boxes that hold several tags together so you can move, style, or name them as a unit:

```html
<h2>Our Menu</h2>
<ul>
  <li>Bread</li>
  <li>Milk</li>
</ul>
<h2>Prices</h2>
<table>…</table>
```

Which parts belong together? Without containers, CSS and screen readers see one flat list. `div` and `section` fix that.

## Tag reference

### `<div>`,generic block container

A block-level box with **no meaning**. Use it to group things for styling or scripting:

```html
<div class="card">
  <h2>Bread</h2>
  <p>Fresh daily.</p>
</div>
```

- `class` names the group for CSS (`"card"` can repeat on many boxes).
- `id` names one unique box on the page (`id="prices"` can appear only once, and links can jump to it: `<a href="#prices">`).

```html
<div id="prices">
  <h2>Prices</h2>
  <p>Updated weekly.</p>
</div>
```

### `<section>`,thematic group

A `section` is a `div` **with meaning**: a themed chunk of the page,like a chapter in a book. Rule: **every `<section>` needs a heading** (`h1`–`h6`) as its first child:

```html
<section>
  <h2>Our Menu</h2>
  <ul>
    <li>Bread</li>
    <li>Milk</li>
  </ul>
</section>
```

No heading? Use `<div>`,not `<section>`:

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

### `<span>`,inline div

`span` is to inline content what `div` is to block content: a meaning-free wrapper inside a sentence:

```html
<p>Result: <span class="price">$1</span></p>
```

| Container | Block or inline? | Meaning? | Rule |
|-----------|------------------|----------|------|
| `div` | Block | None | Group for styling/scripting |
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

Containers nest,inner closes before outer,like all HTML:

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

## Gotchas

- Don't use `div` where a precise tag fits: a list of items is `<ul>`,not `<div>`s; tabular data is `<table>`,not `<div>`s.
- Don't wrap every single element in a `div`,group things that belong together,extra boxes add noise for readers and CSS.
- `id` values must be unique per page; `class` values may repeat.
- `<div>` cannot go inside `<p>`,the browser will close the paragraph early. `<span>` can.

## Recap

| Tag | Job | Watch out |
|-----|-----|-----------|
| `div` | Generic block group | No meaning, needs `class`/`id` to be useful |
| `section` | Themed group | Must have a heading, else use `div` |
| `span` | Generic inline group | Inside sentences only |

**Next:** [18,Page Landmarks](18-landmarks.md) · **Prev:** [16,Forms Basics](16-forms-basics.md)
