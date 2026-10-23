# Grouping Content

As a page grows, you need to group related content. HTML has two block containers, `<div>` and `<section>`, and one inline container, `<span>`. They look similar in the browser but mean different things.

## `<div>`: a generic block

`<div>` groups content without saying what the group is:

```html
<div>
  <h2>About us</h2>
  <p>We teach students how to build websites.</p>
</div>
```

Use `<div>` when no more specific element describes the group. It is common for layout and for CSS or JavaScript hooks.

A `<div>` can contain headings, paragraphs, links, and other blocks:

```html
<div class="contact">
  <h2>Contact</h2>
  <p>Email: <a href="mailto:webclub@example.com">webclub@example.com</a></p>
</div>
```

## `<section>`: a thematic section

`<section>` groups content that forms a distinct part of the document:

```html
<section>
  <h2>Our courses</h2>
  <p>We teach HTML, CSS, and JavaScript.</p>
</section>
```

The difference from `<div>` is meaning. A `<section>` says "this is a section of the page", not just "these elements are grouped".

A section usually has a heading. Without a heading, it is hard for readers and assistive technology to know what the section is for. If the group has no heading and no semantic meaning, use a `<div>`.

## `<span>`: a generic inline container

`<span>` groups a small piece of content inside a line:

```html
<p>My favourite language is <span class="highlight">Python</span>.</p>
```

`<span>` does not start a new line. Use it when you need to style or target part of a sentence. Without a class, `id`, or script, a `<span>` does nothing.

## Choosing between them

| Element | Display | Meaning | Use when |
|---------|---------|---------|----------|
| `<section>` | Block | A distinct thematic section | The content has its own heading and topic |
| `<div>` | Block | No semantic meaning | You need a generic block for layout or styling |
| `<span>` | Inline | No semantic meaning | You need to target part of a line |

If the content is a page header, navigation, main content, article, sidebar, or footer, use the semantic landmarks from the next chapter instead of a `<div>`.

## Classes and ids

Grouping elements become more useful with `class` and `id`.

A class can be shared by several elements:

```html
<section class="course">
  <h2>HTML</h2>
</section>

<section class="course">
  <h2>CSS</h2>
</section>
```

An `id` identifies one element:

```html
<div id="main-content">
  <h1>Welcome</h1>
</div>
```

Use classes for styling groups and ids for in-page links or JavaScript hooks. Do not use the same `id` twice on a page.

## A complete example

```html
<section>
  <h2>Our courses</h2>

  <div class="course">
    <h3>HTML</h3>
    <p>Learn how to structure a <span class="term">web page</span>.</p>
  </div>

  <div class="course">
    <h3>CSS</h3>
    <p>Learn how to style the <span class="term">same page</span>.</p>
  </div>
</section>
```

- `<section>` groups the courses section.
- Each `<div>` groups one course.
- Each `<span>` marks a phrase inside a paragraph.

The `<div>` elements could be `<article>` elements because each course is a self-contained item. The next chapter explains when that is a better choice.

## Exercise: choose the wrapper

For each item, choose `<section>`, `<div>`, or `<span>` and explain why:

1. A group of three news stories, each with its own heading.
2. A wrapper that only exists to apply a grid layout.
3. The word "sold out" inside a product paragraph.
4. A "Contact us" block with a heading and two paragraphs.

Check your answers against these questions:

- Does the group have its own heading and topic?
- Is the group only needed for layout or styling?
- Is the content inline or block-level?

Next: [Page Landmarks](18-landmarks.md)
