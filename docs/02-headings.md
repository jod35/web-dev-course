# What Are Headings?

Headings are how we **introduce and organize sections** on a page. Think of them as the outline you'd scribble before writing an essay, just baked into HTML.

There are six of them:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

`<h1>` is the top-level heading, `<h6>` the deepest. Most pages live happily on just the first two or three.

---

## 1. The `<h1>`: main heading

`<h1>` is the big picture, what the whole page is about.

```html
<h1>Introduction to HTML</h1>
```

A typical start might be:

```html
<h1>Introduction to HTML</h1>

<p>
    HTML is the language used to structure content on the web.
</p>
```

That `<h1>` tells anyone skimming (and any screen reader) what they're about to read.

---

## 2. The `<h2>`: major sections

`<h2>` breaks the main topic into big chunks.

```html
<h1>Introduction to HTML</h1>

<h2>HTML Elements</h2>

<p>
    HTML elements are the building blocks of webpages.
</p>

<h2>HTML Attributes</h2>

<p>
    Attributes provide additional information about HTML elements.
</p>
```

Visualised:

```text
Introduction to HTML
│
├── HTML Elements
│
└── HTML Attributes
```

So `<h1>` is the book title; `<h2>`s are the chapter titles.

---

## 3. The `<h3>`: subsections

Need to go deeper under an `<h2>`? That's `<h3>`.

```html
<h1>Introduction to HTML</h1>

<h2>HTML Elements</h2>

<p>
    HTML elements provide structure to webpages.
</p>

<h3>Headings</h3>

<p>
    Headings are used to organize sections of content.
</p>

<h3>Paragraphs</h3>

<p>
    Paragraphs contain blocks of text.
</p>
```

Hierarchy:

```text
Introduction to HTML       <h1>
│
└── HTML Elements          <h2>
    │
    ├── Headings           <h3>
    │
    └── Paragraphs         <h3>
```

---

## 4. `<h4>`, `<h5>`, and `<h6>`: when you really need depth

They work the same way, just deeper:

```html
<h1>Web Development</h1>

<h2>Frontend Development</h2>

<h3>HTML</h3>

<h4>Text Elements</h4>

<h5>Emphasis</h5>

<h6>Strong Importance</h6>
```

```text
Web Development              h1
│
└── Frontend Development     h2
    │
    └── HTML                 h3
        │
        └── Text Elements    h4
            │
            └── Emphasis     h5
                │
                └── Strong Importance  h6
```

Honestly, most sites you'll build at Migadde will use `<h1>`–`<h3>` and stop there. The lower levels are for docs with a lot of nesting.

---

## 5. Headings Are About Hierarchy, Not Size

It's tempting to pick headings because "h2 looks nice and big." Don't.

They describe **how sections relate**, not how big the text should be.

```html
<h1>Learning Web Development</h1>

<h2>HTML</h2>

<h3>Elements</h3>

<h3>Attributes</h3>

<h2>CSS</h2>

<h3>Selectors</h3>

<h3>Properties</h3>
```

That means:

```text
Learning Web Development
│
├── HTML
│   ├── Elements
│   └── Attributes
│
└── CSS
    ├── Selectors
    └── Properties
```

The levels carry the structure, even if CSS later makes them all look similar.

---

## 6. Headings + Paragraphs

Usually a heading introduces whatever paragraphs follow it:

```html
<h2>HTML Tables</h2>

<p>
    Tables allow us to organize information into rows and columns.
</p>

<p>
    A table can contain headings, rows, and individual data cells.
</p>
```

```text
HTML Tables
    ↓
Paragraph
    ↓
Paragraph
```

The heading sets expectations; the paragraphs deliver.

---

## 7. Don't Pick a Heading for Its Size

We've all done this:

```html
<h3>This is a big title</h3>
```

...just because we liked how `<h3>` looks by default. Use the level that matches the structure instead:

```html
<h1>Main Heading</h1>
```
for the page title,

```html
<h2>Major Section</h2>
```
for a section beneath it,

```html
<h3>Subsection</h3>
```
for something inside that section.

Want it bigger or smaller? That's CSS's job:

```css
h2 {
    font-size: 2rem;
}
```

---

## 8. Try Not to Skip Levels

This isn't invalid, but it usually means the outline wasn't thought through:

```html
<h1>Web Development</h1>

<h3>HTML</h3>
```

There's an `<h2>` missing in between. Clearer:

```html
<h1>Web Development</h1>

<h2>HTML</h2>
```

And if HTML itself has sub-topics:

```html
<h1>Web Development</h1>

<h2>HTML</h2>

<h3>Elements</h3>

<h3>Attributes</h3>
```

Think hierarchy, not font-size ladder.

---

## 9. You Don't Have to Use Every Level

This is perfectly fine:

```html
<h1>My Website</h1>

<h2>About Me</h2>

<h2>Projects</h2>

<h2>Contact</h2>
```

No `<h3>` needed if there are no subsections. Let the content dictate the levels.

---

## 10. A Real-World Example

Say we're putting together a page about Python:

```html
<h1>Learning Python</h1>

<p>
    Python is a general-purpose programming language used in many areas
    of software development.
</p>

<h2>Python Basics</h2>

<p>
    Python provides several fundamental features that beginners should
    understand.
</p>

<h3>Variables</h3>

<p>
    Variables allow programs to store and work with values.
</p>

<h3>Functions</h3>

<p>
    Functions allow us to organize reusable pieces of code.
</p>

<h2>Object-Oriented Programming</h2>

<p>
    Python supports object-oriented programming through classes and objects.
</p>

<h3>Classes</h3>

<p>
    Classes provide a way to define the structure and behaviour of objects.
</p>
```

Structure:

```text
Learning Python                 h1
│
├── Python Basics               h2
│   ├── Variables               h3
│   └── Functions               h3
│
└── Object-Oriented Programming h2
    └── Classes                 h3
```

Much more meaningful than just making some text bigger than other text.

---

## 11. Headings Help Everyone Navigate: Especially Screen Readers

A screen reader can pull out your headings and let a user jump between:

```text
About Us
Services
Products
Contact
```

That's only useful if the headings reflect the actual structure, not just visual styling. So it's both a design and an accessibility habit.

---

## 12. Headings vs Page Titles

They look similar but do different jobs.

In `<head>`:

```html
<head>
    <title>Learning HTML</title>
</head>
```

Visible on the page:

```html
<body>
    <h1>Learning HTML</h1>
</body>
```

* `<title>` describes the document for the browser tab and search results: you won't see it in the page body.
* `<h1>` is the visible headline for readers on the page itself.

---

## Quick Reference

| Element | Use for            |
| ------- | ------------------ |
| `<h1>`  | Main page heading  |
| `<h2>`  | Major section      |
| `<h3>`  | Subsection         |
| `<h4>`  | Smaller subsection |
| `<h5>`  | Deeper subsection  |
| `<h6>`  | Lowest level       |

The takeaway:

> **Heading levels describe what your content *is*, not how big it should look.**

A tidy page often looks like:

```text
<h1>Page Topic</h1>
    │
    ├── <h2>Section</h2>
    │       ├── <h3>Subsection</h3>
    │       └── <h3>Subsection</h3>
    │
    └── <h2>Section</h2>
            └── <h3>Subsection</h3>
```

Use them to make your content easier to **understand, navigate and maintain**, for you, for search engines, and for the next person who reads your code.
