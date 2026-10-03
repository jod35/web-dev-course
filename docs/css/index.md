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

## Chapters at a glance — web.dev order, simpler titles

| Chapter | You will get comfortable with |
|---------|-------------------------------|
| [What is CSS?](01-what-is-css.md) | What CSS does, where to write it, and the rule shape |
| [Box Model](02-box-model.md) | Content, padding, border, margin, `box-sizing` |
| [Selectors](03-selectors.md) | Type, class, id, attribute, and combinators |
| [Nesting](04-nesting.md) | Nesting selectors with `&` |
| [The Cascade](05-cascade.md) | Source order and importance |
| [Specificity](06-specificity.md) | The `[id,class,type]` score |
| [Inheritance](07-inheritance.md) | What inherits and how to control it |
| [Color](08-color.md) | `hex`, `rgb`, `hsl`, `currentColor` |
| [Sizing](09-sizing.md) | `px`, `rem`, `%`, `vw`/`vh`, `min()`/`clamp()` |
| [Layout](10-layout.md) | Flow, positioning, and choosing a mode |
| [Flexbox](11-flexbox.md) | One-dimensional layout with `flex` |
| [Grid](12-grid.md) | Two-dimensional layout with `grid` |
| [Logical Properties](13-logical-properties.md) | `inline`/`block` vs `left`/`right` |
| [Custom Properties](14-custom-properties.md) | Variables with `var()` |
| [Spacing](15-spacing.md) | Scale, `padding` vs `margin` vs `gap` |
| [Pseudo-elements](16-pseudo-elements.md) | `::before`, `::after`, `::first-line` |
| [Pseudo-classes](17-pseudo-classes.md) | `:hover`, `:focus-visible`, `:nth-child` |
| [Borders](18-borders.md) | `border`, `border-radius`, `outline` |
| [Shadows](19-shadows.md) | `box-shadow` and `text-shadow` |
| [Typography](20-typography.md) | Fonts, sizes, and readable type |
| [Responsive](21-responsive.md) | Media queries and mobile-first |
| [Functions](22-functions.md) | `calc()`, `min()`, `max()`, `clamp()` |
| [Practice](23-practice.md) | A complete page with HTML and CSS |

> HTML describes what things are. CSS describes how they look. Keep that split in mind and both languages get simpler.
