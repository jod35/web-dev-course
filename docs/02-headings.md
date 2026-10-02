# What Are Headings?

HTML headings are used to **introduce and organize sections of content** on a webpage.

HTML provides six heading elements:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

They range from `<h1>`, the highest level of heading, to `<h6>`, the lowest.

---

## 1. The `<h1>` Heading

`<h1>` represents the **main heading** of a page or document.

```html
<h1>Introduction to HTML</h1>
```

A page about HTML might begin with:

```html
<h1>Introduction to HTML</h1>

<p>
    HTML is the language used to structure content on the web.
</p>
```

The `<h1>` tells the reader what the overall page is about.

---

## 2. The `<h2>` Heading

`<h2>` represents a **major section** within the main topic.

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

The structure is:

```text
Introduction to HTML
│
├── HTML Elements
│
└── HTML Attributes
```

`<h1>` is the main topic, while the `<h2>` elements introduce major sections.

---

## 3. The `<h3>` Heading

`<h3>` is used for a subsection within an `<h2>` section.

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

The hierarchy is:

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

## 4. `<h4>`, `<h5>`, and `<h6>`

The remaining headings are used for increasingly deeper levels of structure.

```html
<h1>Web Development</h1>

<h2>Frontend Development</h2>

<h3>HTML</h3>

<h4>Text Elements</h4>

<h5>Emphasis</h5>

<h6>Strong Importance</h6>
```

This creates a hierarchy:

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

In practice, most webpages primarily use `<h1>`, `<h2>`, and `<h3>`. The deeper levels are useful when a document has a more complex structure.

---

## 5. Headings Create a Hierarchy

Heading levels are not simply different font sizes.

They describe the **relationship between sections of content**.

For example:

```html
<h1>Learning Web Development</h1>

<h2>HTML</h2>

<h3>Elements</h3>

<h3>Attributes</h3>

<h2>CSS</h2>

<h3>Selectors</h3>

<h3>Properties</h3>
```

This represents:

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

The heading levels communicate this structure.

---

## 6. Headings and Paragraphs

Headings normally introduce the content that follows them.

```html
<h2>HTML Tables</h2>

<p>
    Tables allow us to organize information into rows and columns.
</p>

<p>
    A table can contain headings, rows, and individual data cells.
</p>
```

Here:

```text
HTML Tables
    ↓
Paragraph
    ↓
Paragraph
```

The heading tells the reader what the following paragraphs are about.

---

## 7. Do Not Choose Headings Based on Size

A common beginner mistake is choosing `<h1>`, `<h2>`, or `<h3>` because of how large the text appears.

For example:

```html
<h3>This is a big title</h3>
```

You should not use `<h3>` simply because you like its default size.

The correct heading should be chosen based on the **structure of the content**.

If something is the main heading, use:

```html
<h1>Main Heading</h1>
```

If something is a major section under it, use:

```html
<h2>Major Section</h2>
```

If it is a subsection, use:

```html
<h3>Subsection</h3>
```

If you want to change the appearance, use CSS.

```css
h2 {
    font-size: 2rem;
}
```

---

## 8. Avoid Skipping Heading Levels Without a Reason

Consider:

```html
<h1>Web Development</h1>

<h3>HTML</h3>
```

There is no `<h2>` between them.

This does not necessarily make the HTML invalid, but it usually indicates that the document hierarchy has not been planned correctly.

A clearer structure would be:

```html
<h1>Web Development</h1>

<h2>HTML</h2>
```

If HTML has subsections:

```html
<h1>Web Development</h1>

<h2>HTML</h2>

<h3>Elements</h3>

<h3>Attributes</h3>
```

Think about heading levels as a hierarchy rather than a sequence of font sizes.

---

## 9. Headings Do Not Have to Be Numbered

HTML does not require you to use every heading level.

For example, this is perfectly reasonable:

```html
<h1>My Website</h1>

<h2>About Me</h2>

<h2>Projects</h2>

<h2>Contact</h2>
```

You do not need an `<h3>` if there are no subsections.

The important thing is that the hierarchy accurately represents the content.

---

## 10. A Real-World Example

Imagine a webpage about programming.

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

The structure is:

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

This is much more meaningful than simply making some text large and some text small.

---

## 11. Headings Improve Accessibility

Headings are also important for people who use assistive technologies.

A screen reader can use headings to help a user understand the structure of a webpage and navigate between sections.

For example, a user may want to quickly move between:

```text
About Us
Services
Products
Contact
```

Properly structured headings make this possible.

This is another reason why headings should represent the **actual structure of the document**, rather than being used only for visual styling.

---

## 12. Headings Are Different From Page Titles

A webpage can have a document title inside `<title>`:

```html
<head>
    <title>Learning HTML</title>
</head>
```

And a visible main heading:

```html
<body>
    <h1>Learning HTML</h1>
</body>
```

These serve different purposes.

### `<title>`

The `<title>` describes the webpage as a browser document. It can appear in the browser tab and other contexts.

### `<h1>`

The `<h1>` is visible page content and represents the main heading of the page.

---

## Quick Reference

| Element | Purpose              |
| ------- | -------------------- |
| `<h1>`  | Main heading         |
| `<h2>`  | Major section        |
| `<h3>`  | Subsection           |
| `<h4>`  | Smaller subsection   |
| `<h5>`  | Deeper subsection    |
| `<h6>`  | Lowest heading level |

The important idea is:

> **Heading levels describe the structure of your content, not its visual size.**

A well-structured webpage might look like:

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

Use headings to make your content easier to **understand, navigate, and maintain**.
