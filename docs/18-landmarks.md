# Page Landmarks

HTML has elements that describe the purpose of each part of a page. They help screen readers, search engines, and anyone reading your code.

## A typical page

```html
<body>
  <header>
    <h1>MHSM Web Club</h1>
  </header>

  <nav>
    <a href="index.html">Home</a>
    <a href="projects.html">Projects</a>
    <a href="contact.html">Contact</a>
  </nav>

  <main>
    <article>
      <h2>Our first project</h2>
      <p>The club built a page for the school library.</p>
    </article>

    <aside>
      <h2>Related</h2>
      <p>Read about the CSS track next.</p>
    </aside>
  </main>

  <footer>
    <p>&copy; 2026 MHSM Web Club</p>
  </footer>
</body>
```

Each element tells the browser something about its content. The layout is still controlled by CSS.

## `<header>`

`<header>` holds introductory content for a page or section: a title, logo, or short introduction.

```html
<header>
  <h1>MHSM Web Club</h1>
  <p>Student projects from Makerere High School Migadde.</p>
</header>
```

A header can also belong to an article:

```html
<article>
  <header>
    <h2>Our first project</h2>
    <p>Published 1 October 2026</p>
  </header>
  <p>The club built a page for the school library.</p>
</article>
```

The inner header belongs to the article, not the whole page.

## `<nav>`

`<nav>` wraps major navigation links:

```html
<nav>
  <a href="index.html">Home</a>
  <a href="projects.html">Projects</a>
  <a href="contact.html">Contact</a>
</nav>
```

Use it for the main site navigation, a table of contents, or another important group of links. Do not wrap every link in `<nav>`. A link inside a paragraph is just a link.

## `<main>`

`<main>` holds the primary content of the page:

```html
<main>
  <h1>About the club</h1>
  <p>The club meets every Wednesday after school.</p>
</main>
```

Use one `<main>` per page. Do not put the site navigation, header, or footer inside it.

## `<footer>`

`<footer>` holds information about the page or section: copyright, contact details, or related links.

```html
<footer>
  <p>&copy; 2026 MHSM Web Club</p>
  <a href="contact.html">Contact us</a>
</footer>
```

Like `<header>`, it can belong to the page or to an article.

## `<article>`

`<article>` is for a self-contained piece of content that would still make sense on its own:

- a blog post,
- a news story,
- a forum post,
- a product review.

```html
<article>
  <h2>Library page launched</h2>
  <p>The new page lists opening hours and available books.</p>
</article>
```

A page can contain several articles:

```html
<main>
  <h1>Club news</h1>

  <article>
    <h2>Library page launched</h2>
    <p>The new page lists opening hours and available books.</p>
  </article>

  <article>
    <h2>New members welcome</h2>
    <p>The club meets every Wednesday after school.</p>
  </article>
</main>
```

## `<aside>`

`<aside>` is for content related to the main content but not part of it: a sidebar, related links, or a short note.

```html
<aside>
  <h2>Related</h2>
  <p>Read the CSS track to learn how to style this page.</p>
</aside>
```

Inside an article, an aside might hold a definition or a related fact. If the content is essential to understanding the page, it belongs in the main content instead.

## Section or article?

- `<section>` groups content by topic. It is a part of the page.
- `<article>` is a self-contained piece that could be published on its own.

```html
<main>
  <section>
    <h2>Latest articles</h2>

    <article>
      <h3>Library page launched</h3>
      <p>The new page lists opening hours and available books.</p>
    </article>

    <article>
      <h3>New members welcome</h3>
      <p>The club meets every Wednesday after school.</p>
    </article>
  </section>
</main>
```

The section groups the latest articles. Each article is an independent piece inside that group.

## Semantic HTML compared with div soup

You could build the same page with only `<div>` elements:

```html
<div>
  <div>
    <h1>MHSM Web Club</h1>
  </div>
  <div>
    <a href="index.html">Home</a>
    <a href="projects.html">Projects</a>
  </div>
  <div>
    <h2>Library page launched</h2>
    <p>The new page lists opening hours.</p>
  </div>
</div>
```

It renders, but it does not say what each part is. Compare:

```html
<header>
  <h1>MHSM Web Club</h1>
</header>
```

The second version tells the browser and screen reader that this is the page header.

## Exercise: convert a div-only page

Rewrite this page using `<header>`, `<nav>`, `<main>`, `<article>`, `<aside>`, and `<footer>`:

```html
<div>
  <div>
    <h1>MHSM Web Club</h1>
  </div>

  <div>
    <a href="index.html">Home</a>
    <a href="projects.html">Projects</a>
  </div>

  <div>
    <h2>Library page launched</h2>
    <p>The new page lists opening hours and available books.</p>
  </div>

  <div>
    <p>&copy; 2026 MHSM Web Club</p>
  </div>
</div>
```

Check that:

- there is one `<main>`,
- the navigation is inside `<nav>`,
- the article has its own heading,
- the copyright line is inside `<footer>`,
- no `<div>` remains unless it is needed for layout.

## Reference

| Element | Purpose |
|---------|---------|
| `<header>` | Introductory content for a page or section |
| `<nav>` | Major navigation links |
| `<main>` | Primary content of the page |
| `<article>` | Self-contained content |
| `<aside>` | Related but secondary content |
| `<footer>` | Footer information for a page or section |

Next: continue with the [CSS course](css/index.md).
