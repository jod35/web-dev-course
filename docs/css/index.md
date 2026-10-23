# CSS Course

HTML gives a page structure and meaning. CSS controls how that structure looks: colour, type, spacing, and layout.

This track follows the HTML course. You will use the same `index.html` file and add a separate stylesheet.

[Start with What is CSS?](01-what-is-css.md){ .md-button }

## Before you start

You should be able to build a simple HTML page with headings, paragraphs, links, and images. If not, work through the [HTML course](../00-index.md) first.

You need a folder containing an HTML file and a CSS file. Keep them in the same folder so the path is easy to manage.

## Linking a stylesheet

Add this line inside `<head>`:

```html
<link rel="stylesheet" href="styles.css">
```

The `href` must match the CSS file name exactly. If the file is in a folder, include the folder in the path:

```html
<link rel="stylesheet" href="css/styles.css">
```

If the styles do not appear, check the file name and path first. That is the most common mistake.

## How to use this track

- Type the examples instead of copying them.
- Change one value at a time and reload the browser.
- Use the browser's developer tools to inspect the element and see which CSS rules apply.
- Keep a small project open while you read. The practice chapters make more sense when you have a page to style.

## Chapters

The chapter numbers are the recommended order. The groups below match that order.

### Foundations

- [What is CSS?](01-what-is-css.md): rules, declarations, and where to put CSS.
- [Box Model](02-box-model.md): content, padding, border, margin, and `box-sizing`.
- [Selectors](03-selectors.md): type, class, id, attribute, and combinators.
- [Nesting](04-nesting.md): write related selectors inside one rule.

### How CSS is applied

- [The Cascade](05-cascade.md): source order, origins, and importance.
- [Specificity](06-specificity.md): which selector wins.
- [Inheritance](07-inheritance.md): which properties flow from parent to child.

### Values and colour

- [Color](08-color.md): hex, rgb, hsl, and `currentColor`.
- [Sizing](09-sizing.md): px, rem, em, percentages, and viewport units.

### Layout

- [Layout](10-layout.md): normal flow and positioning.
- [Flexbox](11-flexbox.md): one-dimensional layout.
- [Grid](12-grid.md): two-dimensional layout.
- [Logical Properties](13-logical-properties.md): `inline` and `block` instead of left and right.

### Reusable values and spacing

- [Custom Properties](14-custom-properties.md): reusable values with `var()`.
- [Spacing](15-spacing.md): padding, margin, gap, and a spacing scale.

### Appearance

- [Pseudo-elements](16-pseudo-elements.md): `::before`, `::after`, and text fragments.
- [Pseudo-classes](17-pseudo-classes.md): `:hover`, `:focus-visible`, and structural states.
- [Borders](18-borders.md): width, style, colour, and radius.
- [Shadows](19-shadows.md): `box-shadow` and `text-shadow`.

### Typography and responsive design

- [Typography](20-typography.md): fonts, sizes, and readable text.
- [Responsive](21-responsive.md): fluid layouts and media queries.

### Finishing

- [Functions](22-functions.md): `calc()`, `min()`, `max()`, and `clamp()`.
- [Practice: Build a Page](23-practice.md): put the whole track together.

## What you should be able to do at the end

- Link a stylesheet and explain why a rule is not applying.
- Use classes and a small set of reusable values.
- Build a page layout with flexbox or grid.
- Make text readable and colour contrast accessible.
- Adjust a page for narrow screens without duplicating all your CSS.

CSS describes presentation. HTML still describes meaning. Keep that split and both languages stay simpler.
