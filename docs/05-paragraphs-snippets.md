# Text Blocks

This is a syntax reference for the three block elements you will use most often.

## `<p>`

```html
<p>Fresh bread is baked daily.</p>
```

- Has an opening and closing tag.
- Starts a new block.
- Browsers add vertical space above and below it.
- Do not put block elements such as another `<p>` or a `<div>` inside it.

## `<br>`

```html
<p>
  MHSM Bakery<br>
  Migadde, Uganda<br>
  +256 700 000 000
</p>
```

- Void element: no closing tag.
- Breaks a line inside the current block.
- Use it for addresses, poems, and short lines that belong together.
- Do not use it to create margin or padding.

## `<hr>`

```html
<p>Term one menu</p>
<hr>
<p>Term two menu</p>
```

- Void element: no closing tag.
- Represents a change of topic or scene.
- The browser draws a line by default, but you can style it.
- Do not use several `<hr>` elements in a row for decoration.

## Reference

| Element | Closing tag | Meaning | Common mistake |
|---------|-------------|---------|----------------|
| `<p>` | Yes, `</p>` | A block of text about one idea | Using it for layout |
| `<br>` | No | A line break inside a block | Stacking several to fake spacing |
| `<hr>` | No | A thematic break between sections | Using it as a divider |

## Exercise: clean up the markup

The page below uses the right tags in the wrong places. Rewrite it so the spacing comes from paragraphs, the address uses a line break, and the `<hr>` separates two topics.

```html
<h1>MHSM Bakery</h1>

<p>We bake bread every morning.</p>
<br>
<br>
<br>

<p>Migadde, Uganda<br>Open 7am to 6pm</p>

<hr>

<hr>

<p>Holiday hours: 8am to noon.</p>
```

Check your version by opening it in the browser. There should be three clear ideas: the bakery, the contact details, and the holiday notice. The `<hr>` should appear once, between the contact details and the holiday notice.

Next: [Build Your First Page](06-combined-structure.md)
