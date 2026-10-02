# Page Landmarks: header, nav, main, footer, article, aside

**Goal:** Learn how to divide a web page into meaningful areas using semantic HTML elements.

HTML provides several elements that describe the **role of different parts of a page**.

Instead of using `<div>` for everything, we can use elements such as `<header>`, `<nav>`, `<main>`, and `<footer>` to tell browsers, search engines, screen readers, and other tools what each part of the page represents.

---

## A typical page structure

A simple web page might look like this:

```html
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main>

        <article>
            <h2>Learning HTML</h2>
            <p>HTML is used to structure web pages.</p>
        </article>

        <aside>
            <h2>Related Topics</h2>
            <p>Learn about CSS and JavaScript next.</p>
        </aside>

    </main>

    <footer>
        <p>Copyright 2026 My Website</p>
    </footer>

</body>
```

The important idea is that each element tells us **what the content is for**, not just how it should look.

---

## `<header>`

The `<header>` element contains introductory content for a page or a section.

```html
<header>
    <h1>My Website</h1>
    <p>Learn web development</p>
</header>
```

A page header might contain:

* A website logo
* The website name
* A heading
* Introductory information
* Navigation

For example:

```html
<header>
    <h1>Uganda Travel Guide</h1>
    <p>Discover places to visit in Uganda.</p>
</header>
```

### Important

`<header>` does not necessarily mean the very top of the entire page.

It can also be used inside another semantic element.

```html
<article>

    <header>
        <h2>10 Places to Visit in Uganda</h2>
        <p>Published on October 1, 2026</p>
    </header>

    <p>Uganda has many interesting places to visit...</p>

</article>
```

Here, the `<header>` belongs to the `<article>`.

---

## `<nav>`

The `<nav>` element contains important navigation links.

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
</nav>
```

It is commonly used for:

* Main website navigation
* Section navigation
* A table of contents
* Other major groups of navigation links

For example:

```html
<nav>
    <a href="index.html">Home</a>
    <a href="courses.html">Courses</a>
    <a href="projects.html">Projects</a>
    <a href="contact.html">Contact</a>
</nav>
```

### `<nav>` does not mean every link

Not every group of links needs to be inside `<nav>`.

For example:

```html
<p>
    Read our <a href="privacy.html">privacy policy</a>.
</p>
```

This does not need a `<nav>` element.

Use `<nav>` when the links form an important navigation area.

---

## `<main>`

The `<main>` element contains the **main content of the page**.

```html
<main>
    <h1>Learning HTML</h1>

    <p>
        HTML is the language used to structure web pages.
    </p>
</main>
```

A typical page might have:

```html
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <nav>
        <a href="/">Home</a>
        <a href="/about.html">About</a>
    </nav>

    <main>
        <h2>Welcome</h2>
        <p>This is the main content.</p>
    </main>

    <footer>
        <p>Copyright 2026</p>
    </footer>

</body>
```

### Important rule

A page should normally have **one `<main>` element** representing the primary content.

Content that appears repeatedly across pages, such as navigation or a site footer, generally does not belong inside `<main>`.

---

## `<footer>`

The `<footer>` element contains information about the page or a section.

A page footer might contain:

* Copyright information
* Contact information
* Links
* Author information
* Related information

Example:

```html
<footer>
    <p>Copyright 2026 My Website</p>
    <a href="contact.html">Contact us</a>
</footer>
```

Like `<header>`, a `<footer>` can belong to the whole page or to a specific section.

For example:

```html
<article>

    <h2>Learning HTML</h2>

    <p>HTML gives structure to web pages.</p>

    <footer>
        <p>Written by Jonathan</p>
    </footer>

</article>
```

Here, the footer belongs to the article rather than the entire website.

---

## `<article>`

The `<article>` element represents a **self-contained piece of content**.

The content should make sense on its own and could potentially be distributed or reused separately.

Examples include:

* A blog post
* A news article
* A forum post
* A product review
* A comment
* A social media post

Example:

```html
<article>
    <h2>What is HTML?</h2>

    <p>
        HTML is a markup language used to structure
        content on the web.
    </p>
</article>
```

A page can contain multiple articles:

```html
<main>

    <h1>Latest News</h1>

    <article>
        <h2>New School Opens in Kampala</h2>
        <p>The school opened this week...</p>
    </article>

    <article>
        <h2>Local Students Win Competition</h2>
        <p>The students won the competition...</p>
    </article>

</main>
```

Each `<article>` represents a separate piece of content.

---

## `<aside>`

The `<aside>` element contains content that is related to the surrounding content but is not part of its main flow.

It is commonly used for:

* Sidebars
* Related articles
* Author information
* Advertisements
* Additional information
* Related links

Example:

```html
<aside>
    <h2>Related Articles</h2>

    <a href="css.html">Learn CSS</a>
    <a href="javascript.html">Learn JavaScript</a>
</aside>
```

Another example:

```html
<article>
    <h1>Learning HTML</h1>

    <p>
        HTML is used to structure content on the web.
    </p>

    <aside>
        <h2>Did you know?</h2>
        <p>HTML was first introduced in the early 1990s.</p>
    </aside>
</article>
```

The information in the `<aside>` is related to the article but is not part of its main content.

---

## Putting everything together

Here is a more complete page:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My Blog</title>
</head>

<body>

    <header>
        <h1>My Blog</h1>
        <p>Thoughts about technology and programming.</p>
    </header>

    <nav>
        <a href="index.html">Home</a>
        <a href="articles.html">Articles</a>
        <a href="about.html">About</a>
    </nav>

    <main>

        <article>

            <header>
                <h2>Why I Like Python</h2>
                <p>Published on October 1, 2026</p>
            </header>

            <p>
                Python is a programming language known for its
                readable syntax and large ecosystem.
            </p>

            <p>
                It can be used for web development, automation,
                data analysis, and many other tasks.
            </p>

            <footer>
                <p>Written by Jonathan</p>
            </footer>

        </article>

        <aside>
            <h2>Related Articles</h2>

            <a href="fastapi.html">Introduction to FastAPI</a>
            <a href="django.html">Introduction to Django</a>
        </aside>

    </main>

    <footer>
        <p>Copyright 2026 My Blog</p>
    </footer>

</body>

</html>
```

Notice that the page has **two different kinds of headers and footers**:

```text
Page
├── header
│   └── Website introduction
│
├── nav
│   └── Main navigation
│
├── main
│   ├── article
│   │   ├── header
│   │   ├── article content
│   │   └── footer
│   │
│   └── aside
│
└── footer
    └── Website footer
```

The inner `<header>` and `<footer>` belong to the `<article>`, while the outer ones belong to the page.

---

## Semantic HTML vs `<div>`

You could technically build the same page using `<div>` elements:

```html
<div>
    <div>
        <h1>My Blog</h1>
    </div>

    <div>
        <a href="/">Home</a>
        <a href="/articles.html">Articles</a>
    </div>

    <div>
        <div>
            <h2>My Article</h2>
            <p>Article content...</p>
        </div>

        <div>
            <h2>Related</h2>
            <p>Related information...</p>
        </div>
    </div>

    <div>
        <p>Copyright 2026</p>
    </div>
</div>
```

The browser can display this, but the HTML does not clearly communicate what each part means.

Compare:

```html
<div>
    <h1>My Blog</h1>
</div>
```

with:

```html
<header>
    <h1>My Blog</h1>
</header>
```

The second version communicates that this is a header.

This is the purpose of **semantic HTML**.

---

## When to use each element

### `<header>`

Use for introductory content belonging to a page or section.

```html
<header>
    <h1>My Website</h1>
</header>
```

### `<nav>`

Use for an important group of navigation links.

```html
<nav>
    <a href="/">Home</a>
    <a href="/about.html">About</a>
</nav>
```

### `<main>`

Use for the primary content of the page.

```html
<main>
    <h1>About Us</h1>
    <p>We teach programming.</p>
</main>
```

### `<article>`

Use for content that represents a self-contained piece.

```html
<article>
    <h2>My Blog Post</h2>
    <p>...</p>
</article>
```

### `<aside>`

Use for related or supplementary content.

```html
<aside>
    <h2>Related</h2>
    <p>More information...</p>
</aside>
```

### `<footer>`

Use for footer information belonging to a page or section.

```html
<footer>
    <p>Copyright 2026</p>
</footer>
```

---

## The difference between `<section>` and `<article>`

These two elements are often confused.

A `<section>` groups content that belongs to a particular **theme or part of a page**.

An `<article>` represents a **self-contained piece of content**.

For example:

```html
<main>

    <section>
        <h2>Latest Articles</h2>

        <article>
            <h3>Learning Python</h3>
            <p>Python is...</p>
        </article>

        <article>
            <h3>Learning HTML</h3>
            <p>HTML is...</p>
        </article>

    </section>

</main>
```

Here:

* `<section>` groups the latest articles.
* Each `<article>` is an independent piece of content.

---

## Rules

1. Use semantic elements when they accurately describe your content.
2. Use `<main>` for the primary content of the page.
3. Use `<nav>` for important navigation areas.
4. Use `<article>` for self-contained content.
5. Use `<aside>` for related or supplementary content.
6. `<header>` and `<footer>` can belong to the whole page or to individual sections and articles.
7. Do not use these elements simply because they have a particular visual appearance.
8. Use CSS to control how semantic elements look.

---

## Recap

| Element     | Purpose                                    |
| ----------- | ------------------------------------------ |
| `<header>`  | Introductory content for a page or section |
| `<nav>`     | Important navigation links                 |
| `<main>`    | Main content of the page                   |
| `<article>` | Self-contained piece of content            |
| `<aside>`   | Related or supplementary content           |
| `<footer>`  | Footer information for a page or section   |

The main idea is:

```text
<header>   → What introduces this page or section?
<nav>      → Where can I navigate?
<main>     → What is the primary content?
<article>  → What is a self-contained piece?
<aside>    → What is related but secondary?
<footer>   → What information belongs at the end?
```

These elements give your HTML **meaning and structure**, rather than just grouping elements together.
