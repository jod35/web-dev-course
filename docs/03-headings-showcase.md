# 03 - Headings h1–h6 Showcase

**Goal:** In this chapter you will meet all six heading levels and see how their relative sizes compare.

## The rule first

Each page must contain one `<h1>` element. Heading levels must never be skipped, for example from level 1 to level 3.

## All six levels

| Tag | Renders (approx.) | Use for |
|-----|-------------------|---------|
| `<h1>` | **Bakery Homepage** (largest) | Page title, used once |
| `<h2>` | **Our Menu** | Major sections |
| `<h3>` | **Drinks** | Subsections |
| `<h4>` | **Hot Drinks** | Sub-subsections |
| `<h5>` | **Tea Notes** | Deep detail |
| `<h6>` | **Fine print head** (smallest) | Rarely used, deepest level |

## Snippets

```html
<h1>Bakery</h1>
<h2>Our Menu</h2>
<h3>Drinks</h3>
<h4>Hot Drinks</h4>
<h5>Tea Notes</h5>
<h6>Fine print head</h6>
```

The following example shows correct nesting, and you can see that no level has been skipped:

```html
<h1>Bakery</h1>
<h2>Our Menu</h2>
<h3>Drinks</h3>
<h2>Prices</h2>
```

## Rules

- If a page contains two `<h1>` tags, split the page into two pages or demote one of the titles to `<h2>`.
- If an `<h1>` element is followed directly by an `<h3>` element, insert the missing `<h2>` element, even when it feels redundant.
- A paragraph which has been styled to look large is **not** a heading, so screen readers will not list it as one.

<figure markdown="span">

![Image title](./imgs/heading.png){ width="400" }

<figcaption>Headings</figcaption>

</figure>


## Recap

| Level | Size hint | Role |
|-------|-----------|------|
| `h1` | Biggest | Page title, used once |
| `h2` | Large | Sections |
| `h3`–`h6` | Shrinking | Subsections, never skipped |

**Next:** [04 - What Are Paragraphs?](04-paragraphs.md) · **Prev:** [02 - What Are Headings?](02-headings.md)
