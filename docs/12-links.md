# 12 - Links

**Goal:** connect pages with `<a>`,the tag that makes the web a web.

## The tag

`href` holds the destination. The content is the **link text**,it must describe the destination:

```html
<a href="https://example.com/menu">See our menu</a>
```

Never "click here",screen readers list links out of context, and search engines weigh link text.

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
| Relative | path, no scheme | Your own site,portable across domains |
| Anchor | `#` | Element with matching `id` on the page |

## Useful attributes

```html
<a href="https://example.com" target="_blank" rel="noopener">Open in new tab</a>
```

| Attribute | Job |
|-----------|-----|
| `href` | Destination (required) |
| `target="_blank"` | Open in a new tab,use rarely, warn the user |
| `rel="noopener"` | Security partner of `target="_blank"`,always pair them |
| `title` | Extra hint,not a substitute for good link text |

Special schemes:

```html
<a href="mailto:hello@mhsm.web">Email us</a>
<a href="tel:+255700000000">Call us</a>
```

## Gotchas

- Relative links keep working when you move the whole site; absolute links to your own pages break that portability.
- An `<a>` without `href` is not a link,keyboard users can't reach it.
- Images can be links too: wrap `<img>` in `<a>` (Chapter 13), with meaningful `alt`.

## Recap

| Idea | Rule |
|------|------|
| Link text | Describes destination, never "click here" |
| Own pages | Relative URLs |
| New tabs | Rarely, with `rel="noopener"` |
| Anchors | `href="#id"` ↔ `id="id"` |

**Next:** [13,Images](13-images.md) · **Prev:** [11,Special Blocks](11-special-blocks.md)
