# Headings

Headings divide a page into sections. They create the outline that readers, search engines, and screen readers use to understand the page.

HTML has six heading levels:

```html
<h1>Page title</h1>
<h2>Main section</h2>
<h3>Subsection</h3>
<h4>Deeper subsection</h4>
<h5>Usually unnecessary</h5>
<h6>Usually unnecessary</h6>
```

Most pages only need `<h1>`, `<h2>`, and occasionally `<h3>`.

## Start with one `<h1>`

The `<h1>` is the main heading for the page. It should describe the whole page, not just the first paragraph.

```html
<h1>MHSM Bakery</h1>
<p>Fresh bread and pastries, baked on site every morning.</p>
```

Use one `<h1>` per page. If you have two competing main topics, you probably need two pages.

## Use `<h2>` for main sections

An `<h2>` starts a major section under the page title:

```html
<h1>MHSM Bakery</h1>

<h2>Bread</h2>
<p>White, brown, and whole wheat loaves are baked daily.</p>

<h2>Pastries</h2>
<p>Tea buns, doughnuts, and meat pies are available from 7am.</p>
```

The heading tells the reader what the section is about. The paragraph gives the detail.

## Heading levels show hierarchy

The number describes the level of the section, not the size of the text:

```text
MHSM Bakery                  h1
├── Bread                    h2
│   ├── White bread          h3
│   └── Brown bread          h3
└── Pastries                 h2
    ├── Tea buns             h3
    └── Doughnuts            h3
```

Do not jump from `<h1>` to `<h3>` because you want smaller text. If a section belongs under an `<h2>`, use an `<h3>`. If it does not, keep it as an `<h2>`.

```html
<!-- Avoid: the h3 skips a level -->
<h1>MHSM Bakery</h1>
<h3>Bread</h3>

<!-- Better -->
<h1>MHSM Bakery</h1>
<h2>Bread</h2>
<h3>White bread</h3>
```

You do not have to use every level. If there are no subsections, `<h1>` and `<h2>` are enough.

## Headings are not for styling

A common mistake is choosing `<h3>` because it looks smaller than `<h2>`. Heading levels describe structure. CSS controls size.

If you want normal text to look large, style the paragraph:

```html
<p class="lead">Fresh bread is baked every morning.</p>
```

```css
.lead {
  font-size: 1.25rem;
}
```

Changing the size of a heading does not change its level. A visually small `<h1>` is still the main heading.

## Why this matters for accessibility

Screen reader users can list all the headings on a page and jump between them. That only works when the headings form a sensible outline.

```text
MHSM Bakery
  Bread
  Pastries
  Contact
```

Good headings also help sighted readers scan the page and help search engines understand which parts are important.

## Check your work

- Does the page have exactly one `<h1>`?
- Does each `<h2>` introduce a real section?
- Are there any skipped levels, such as `<h1>` followed directly by `<h3>`?
- Would the page still make sense if you only read the headings?

## Try it

Open the page you started in the previous chapter. Add a short menu with:

- one `<h1>` for the bakery name,
- one `<h2>` for bread,
- one `<h2>` for pastries,
- one `<h3>` for a type of bread if you have more than one.

Reload the page. Then remove the text and read only the headings. They should still describe the page.

Next: [Heading Levels](03-headings-showcase.md) is a quick reference and practice page for all six levels.
