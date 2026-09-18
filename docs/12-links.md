# 12 - Links

**Goal:** In this chapter you will learn how to connect pages with the `<a>` element, which is the tag that makes the web a web.

## The tag

The `href` attribute holds the destination, while the element content forms the **link text**, which must describe the destination:

```html
<a href="https://example.com/menu">See our menu</a>
```

Never write "click here" as link text, because screen readers list links out of context and search engines weigh the link text heavily.

## Three kinds of destination

```html
<!-- absolute: another site -->
<a href="https://example.com">Example</a>

<!-- relative: your own site, same folder -->
<a href="menu.html">Menu</a>

<!-- relative: subfolder -->
<a href="docs/prices.html">Prices</a>

<!-- anchor: a spot on the same page -->
<a href="#prices">Jump to prices</a>
<h2 id="prices">Prices</h2>
```

| Form | Starts with | Goes to |
|------|-------------|---------|
| Absolute | `https://` | Another site |
| Relative | Path without a scheme | Your own site, which stays portable across domains |
| Anchor | `#` | The element with the matching `id` on the same page |

## Useful attributes

```html
<a href="https://example.com" target="_blank" rel="noopener">Open in new tab</a>
```

| Attribute | Job |
|-----------|-----|
| `href` | The destination, which is required |
| `target="_blank"` | Opens the link in a new tab, so use it rarely and warn the user |
| `rel="noopener"` | The security partner of `target="_blank"`, so always pair them |
| `title` | An extra hint, which is not a substitute for good link text |

Special schemes:

```html
<a href="mailto:hello@mhsm.web">Email us</a>
<a href="tel:+255700000000">Call us</a>
```

## Rules

- Relative links keep working when you move the whole site, while absolute links to your own pages lose that portability.
- An `<a>` element without an `href` attribute is not a link, and keyboard users cannot reach it.
- Images can serve as links too. When you wrap an `<img>` element in an `<a>` element, as shown in Chapter 13, provide meaningful `alt` text.

## Recap

| Idea | Rule |
|------|------|
| Link text | Describe the destination, and never write "click here" |
| Own pages | Use relative URLs |
| New tabs | Use them rarely, and always include `rel="noopener"` |
| Anchors | Match `href="#id"` with `id="id"` |

**Next:** [13 - Images](13-images.md) · **Prev:** [11 - Special Blocks](11-special-blocks.md)
