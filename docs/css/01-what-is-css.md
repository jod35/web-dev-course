# What is CSS?

CSS controls how HTML looks. A paragraph is still a paragraph, but CSS decides its colour, size, spacing, and position on the page.

## A first rule

```css
p {
  color: #333;
  line-height: 1.6;
}
```

A rule has a selector and a declaration block:

```text
p          selector: which elements to style
{ }        declaration block
color      property
#333       value
```

Read it as: select every `<p>` element, then apply these declarations.

A rule can have several declarations:

```css
h1 {
  font-size: 2rem;
  margin-bottom: 0.5rem;
}
```

## Where CSS lives

### External stylesheet

Put CSS in a separate file and link it from `<head>`:

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

```css
/* styles.css */
body {
  font-family: system-ui, sans-serif;
}
```

This is the normal choice. It keeps HTML readable and lets you reuse the same styles on several pages.

### Internal stylesheet

A `<style>` block inside `<head>` works for small tests:

```html
<style>
  p {
    color: crimson;
  }
</style>
```

Use it for quick experiments, not for a whole site.

### Inline styles

An inline style applies to one element:

```html
<p style="color: crimson;">Hello</p>
```

Avoid inline styles for normal styling. They are hard to reuse and hard to override.

## A starting stylesheet

Start a project with a small reset and readable defaults:

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
  color: #222;
}
```

`box-sizing: border-box` makes width calculations easier. The body rule sets a readable font and removes the browser's default margin.

## Check your work

If your styles do not apply:

- Check the stylesheet path in `href`.
- Check that the CSS file is saved with a `.css` extension.
- Check that the `<link>` is inside `<head>`.
- Check for a missing `}` or `;` in the CSS file.
- Reload the page after saving.

## Try it

1. Create `index.html` and `styles.css` in the same folder.
2. Link the stylesheet from the HTML file.
3. Add a heading and two paragraphs.
4. Change the body font, text colour, and line height in the CSS.
5. Add a rule that makes all links a different colour.

If nothing changes, fix the link before adding more CSS.

Next: [Box Model](02-box-model.md)
