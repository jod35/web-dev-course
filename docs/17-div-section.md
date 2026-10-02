# 17 - Grouping: div, section, span

**Goal:** In this chapter, you will learn how to group HTML content using `<div>`, `<section>`, and `<span>`. Although these elements can all be used to group content, they have different meanings and purposes.

## Why Group Content?

As webpages become larger, we need ways to organize related content.

For example, a page might contain:

```text
Header
    Navigation

Main content
    About us
    Our services

Footer
```

HTML provides different elements for grouping these parts of a webpage.

---

# `<div>` - Generic Block Container

The `<div>` element is a **generic container** for grouping content.

```html
<div>
    <h2>About Us</h2>
    <p>We build software for businesses.</p>
</div>
```

`<div>` does not tell the browser what the content means.

It simply says:

> These elements belong together as a group.

This makes `<div>` useful when there is no more meaningful semantic element that describes the content.

---

## `<div>` as a Container

A `<div>` can contain many different elements.

```html
<div>
    <h2>Student Information</h2>

    <p>Name: Jonathan</p>
    <p>Class: S2</p>

    <a href="profile.html">View Profile</a>
</div>
```

The `<div>` groups all of this content together.

It is commonly used when working with CSS and JavaScript because it provides a convenient element to target.

---

# `<section>` - A Thematic Section

The `<section>` element represents a **thematically related section of content**.

```html
<section>
    <h2>About Us</h2>

    <p>
        We teach students how to build websites.
    </p>
</section>
```

Unlike `<div>`, `<section>` has semantic meaning.

It tells browsers and other tools:

> This is a distinct section of the document.

---

## Sections Usually Have a Heading

A section will commonly have a heading that describes its content.

```html
<section>
    <h2>Our Services</h2>

    <p>We provide web development services.</p>
</section>
```

Another section can follow it:

```html
<section>
    <h2>Contact Us</h2>

    <p>Get in touch with our team.</p>
</section>
```

The headings help users and assistive technologies understand the structure of the page.

---

# `<div>` vs `<section>`

Consider:

```html
<div>
    <h2>About Us</h2>
    <p>We teach programming.</p>
</div>
```

and:

```html
<section>
    <h2>About Us</h2>
    <p>We teach programming.</p>
</section>
```

Both can group the content, but they communicate different things.

### `<div>`

Means:

> This content is grouped together.

### `<section>`

Means:

> This is a distinct section of related content.

Use `<section>` when the content represents a meaningful section of the document.

Use `<div>` when you simply need a generic container and there is no more appropriate semantic element.

---

# `<span>` - Generic Inline Container

The `<span>` element is a generic container for **small pieces of inline content**.

```html
<p>
    My favourite language is
    <span>Python</span>.
</p>
```

Unlike `<div>`, `<span>` does not create a new block.

It stays within the surrounding text.

For example:

```html
<p>Hello <span>Jonathan</span>, welcome!</p>
```

The `<span>` is part of the same paragraph.

---

# `<span>` for Part of a Sentence

A common use of `<span>` is to identify a particular part of some text.

```html
<p>
    The weather today is
    <span>very warm</span>.
</p>
```

The `<span>` does not give the text any special semantic meaning by itself.

It simply provides a way to identify that particular piece of content.

---

# `<span>` vs `<div>`

The main difference is how they participate in the page's flow.

### `<div>`

A block-level container.

```html
<div>
    First group
</div>

<div>
    Second group
</div>
```

The groups normally appear on separate lines.

### `<span>`

An inline container.

```html
<p>
    This is <span>one</span> sentence.
</p>
```

The `<span>` stays within the surrounding line of text.

---

# Grouping with Classes and IDs

These elements are often given `class` or `id` attributes so that they can be identified.

```html
<div class="card">
    <h2>Python</h2>
    <p>A programming language.</p>
</div>
```

A class can be used to identify multiple elements that belong to the same category.

```html
<section class="course">
    <h2>Python Course</h2>
</section>

<section class="course">
    <h2>HTML Course</h2>
</section>
```

An `id` identifies a particular element.

```html
<div id="main-content">
    <h1>Welcome</h1>
</div>
```

Classes and IDs are particularly useful when working with CSS and JavaScript.

---

# Combining the Elements

A webpage can use all three elements together.

```html
<section>

    <h2>Our Courses</h2>

    <div class="course">
        <h3>HTML</h3>
        <p>Learn how to build <span>web pages</span>.</p>
    </div>

    <div class="course">
        <h3>Python</h3>
        <p>Learn how to build <span>programs</span>.</p>
    </div>

</section>
```

Here:

* `<section>` represents the **Courses section**.
* `<div>` groups each individual course.
* `<span>` identifies a small piece of text within a paragraph.

---

# Choosing the Right Element

When grouping content, ask what the group means.

### Use `<section>` when:

The content represents a distinct **thematic section**.

```html
<section>
    <h2>Our Services</h2>
    ...
</section>
```

### Use `<div>` when:

You need a **generic container** and there is no more meaningful semantic element.

```html
<div>
    ...
</div>
```

### Use `<span>` when:

You need to group or identify a **small inline piece of content**.

```html
<p>This is <span>important</span> information.</p>
```

---

# Important Elements

| Element     | Purpose                                                 |
| ----------- | ------------------------------------------------------- |
| `<section>` | Groups thematically related content                     |
| `<div>`     | Generic block-level container                           |
| `<span>`    | Generic inline container                                |
| `class`     | Identifies one or more elements as belonging to a group |
| `id`        | Gives an element a unique identifier                    |

---

# Recap

Remember the difference:

```text
<section>
    A meaningful section of the document
</section>

<div>
    A generic block-level group
</div>

<p>
    Some text with a
    <span>small inline group</span>
    inside it.
</p>
```

A useful way to think about them is:

**`<section>` = meaningful group**

**`<div>` = generic block group**

**`<span>` = generic inline group**
