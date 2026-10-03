# CSS Course: Start Here

CSS is what makes HTML look like a designed page, not a plain document. HTML gives you structure and meaning, CSS controls presentation: colors, spacing, layout, and how things adapt to different screens.

This track follows the HTML course. You already know how to mark up content. Now you will learn how to style it.

## How to use this track

1. **You need the HTML track first.** If you have not gone through the HTML chapters, start there. CSS without HTML is just rules with nothing to apply to.
2. **Type every example.** Make a file `index.html` and a file `styles.css` in the same folder, link them, and open `index.html` in a browser. Change values and reload, that is where learning sticks.
3. Chapters are ordered so each one builds on the last. Chapters marked reference have full detail, skim them first and come back when you need exact syntax.

## Linking CSS to HTML — the one line you will use everywhere

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

```css
/* styles.css */
p {
  color: #333;
  line-height: 1.6;
}
```

If that line is wrong, nothing you write in `styles.css` will show up. Check the filename and the `href` first when styles seem to do nothing.

## Chapters at a glance

| Chapter | You will get comfortable with |
|---------|-------------------------------|
| [What is CSS?](01-what-is-css.md) | What CSS does, where to write it, and the basic rule shape |
| [Selectors](02-selectors.md) | Type, class, id, attribute, pseudo-class and combinators, and how to choose the right one |
| [Cascade & Specificity](03-cascade-specificity.md) | Why one rule wins over another, and how to keep specificity low |
| [Box Model](04-box-model.md) | Content, padding, border, margin, and `box-sizing` |
| [Colors & Units](05-colors-units.md) | `hex`, `rgb`, `hsl`, `rem`, `em`, `%`, `vw`/`vh` and when to use each |
| [Text & Typography](06-text-typography.md) | Fonts, sizes, spacing, and readable type |
| [Flexbox](07-flexbox.md) | One-dimensional layout: rows and columns with `flex` |
| [Grid](08-grid.md) | Two-dimensional layout: real page grids with `grid` |
| [Responsive Design](09-responsive.md) | Media queries, fluid sizing, and mobile-first habits |
| [Putting It Together](10-practice.md) | A small page built with HTML and CSS, end to end |

> HTML describes what things are. CSS describes how they look. Keep that split in mind and both languages get simpler.
