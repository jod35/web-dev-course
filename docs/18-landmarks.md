# Page Landmarks: header, nav, main, footer, article, aside

Instead of wrapping everything in `<div>`, HTML gives us elements that say **what each part of the page is for**. That helps browsers, search engines and screen readers, and it makes your code much easier to follow.

---

## A typical page structure

A straightforward page might look like this:

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

The takeaway: each element tells us the **purpose** of its content, not just how it should look.

---

## `<header>`: Introductory content

Think of `<header>` as the intro for a page or a section:

```html
<header>
    <h1>My Website</h1>
    <p>Learn web development</p>
</header>
```

A site header often holds a logo, site name, heading, or a bit of intro text. For example:

```html
<header>
    <h1>Uganda Travel Guide</h1>
    <p>Discover places to visit in Uganda.</p>
</header>
```

### It doesn't have to be at the very top

`<header>` can also live inside another element:

```html
<article>

    <header>
        <h2>10 Places to Visit in Uganda</h2>
        <p>Published on October 1, 2026</p>
    </header>

    <p>Uganda has many interesting places to visit...</p>

</article>
```

Here the header belongs to the `<article>`, not the whole page.

---

## `<nav>`: Important navigation

`<nav>` wraps **major navigation links**:

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
</nav>
```

Use it for main site nav, section nav, or a table of contents, e.g.:

```html
<nav>
    <a href="index.html">Home</a>
    <a href="courses.html">Courses</a>
    <a href="projects.html">Projects</a>
    <a href="contact.html">Contact</a>
</nav>
```

### Not every link needs `<nav>`

Inline links like this are fine without it:

```html
<p>
    Read our <a href="privacy.html">privacy policy</a>.
</p>
```

Save `<nav>` for genuinely important navigation blocks.

---

## `<main>`: The primary content

`<main>` holds the **core content of that page**:

```html
<main>
    <h1>Learning HTML</h1>

    <p>
        HTML is the language used to structure web pages.
    </p>
</main>
```

A fuller picture:

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

**One `<main>` per page** is the usual rule: and don't put site-wide chrome like nav or footer inside it.

---

## `<footer>`: Closing info

`<footer>` is for information about its page or section, copyright, contacts, related links, author:

```html
<footer>
    <p>Copyright 2026 My Website</p>
    <a href="contact.html">Contact us</a>
</footer>
```

Like `<header>`, it can belong to the page or to a specific article:

```html
<article>

    <h2>Learning HTML</h2>

    <p>HTML gives structure to web pages.</p>

    <footer>
        <p>Written by Jonathan</p>
    </footer>

</article>
```

That footer describes the article, not the entire site.

---

## `<article>`: Self-contained content

`<article>` is for a **standalone piece**, something that would make sense on its own if syndicated:

* a blog post
* a news story
* a forum post or comment
* a product review

```html
<article>
    <h2>What is HTML?</h2>

    <p>
        HTML is a markup language used to structure
        content on the web.
    </p>
</article>
```

You can have several on one page:

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

Each `<article>` is its own independent unit.

---

## `<aside>`: Related but secondary

`<aside>` is for content **related to the surroundings but not part of the main flow**, sidebars, related articles, callouts, quick facts:

```html
<aside>
    <h2>Related Articles</h2>

    <a href="css.html">Learn CSS</a>
    <a href="javascript.html">Learn JavaScript</a>
</aside>
```

Inside an article, for example:

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

It's related to the article, but you could skip it and the main argument would still make sense.

---

## Putting everything together

A more complete example:

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

Notice you've got **two kinds of header/footer** here:

```text
Page
├── header
│   └── Website intro
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
    └── Site footer
```

The inner header/footer belong to the article; the outer ones belong to the page.

---

## Semantic HTML vs `<div>` Soup

You *could* build the same page with only `<div>`s:

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

It renders, but it says nothing about *what* each part is. Compare:

```html
<div>
    <h1>My Blog</h1>
</div>
```

vs.

```html
<header>
    <h1>My Blog</h1>
</header>
```

The second version announces "this is a header", that's the point of **semantic HTML**.

---

## When to use each

**`<header>`**: intro for a page or section:
```html
<header>
    <h1>My Website</h1>
</header>
```

**`<nav>`**: an important group of navigation links:
```html
<nav>
    <a href="/">Home</a>
    <a href="/about.html">About</a>
</nav>
```

**`<main>`**: primary content of the page:
```html
<main>
    <h1>About Us</h1>
    <p>We teach programming.</p>
</main>
```

**`<article>`**: self-contained piece:
```html
<article>
    <h2>My Blog Post</h2>
    <p>...</p>
</article>
```

**`<aside>`**: related / supplementary:
```html
<aside>
    <h2>Related</h2>
    <p>More information...</p>
</aside>
```

**`<footer>`**: footer for a page or section:
```html
<footer>
    <p>Copyright 2026</p>
</footer>
```

---

## `<section>` vs `<article>`: A Quick Distinction

They're easy to mix up:

* `<section>` groups content by **theme**: "these things belong to the same topic/section of the page."
* `<article>` is a **self-contained piece** that could stand alone.

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

* `<section>` = grouping of latest articles.
* Each `<article>` = an independent piece inside that group.

---

## A few ground rules

1. Reach for semantic elements when they actually describe your content, don't force them.
2. Keep one `<main>` for the primary content.
3. Use `<nav>` only for important navigation.
4. Use `<article>` when the content is genuinely self-contained.
5. Use `<aside>` for related but secondary material.
6. Remember `<header>`/`<footer>` can belong to the page *or* to an article/section.
7. Don't pick these elements for how they look, use CSS for presentation.

---

## Recap

| Element | What it's for |
| ------- | ------------- |
| `<header>` | Intro for a page or section |
| `<nav>` | Important navigation |
| `<main>` | Main content of the page |
| `<article>` | Self-contained piece |
| `<aside>` | Related / supplementary content |
| `<footer>` | Footer info for a page or section |

Quick mental check:

```text
<header>  → What's the intro for this page or section?
<nav>     → Where can I navigate?
<main>    → What's the primary content?
<article> → What's a standalone piece?
<aside>   → What's related but secondary?
<footer>  → What belongs at the end?
```

Use them to give your HTML **meaning and structure**, not just boxes to fill.
