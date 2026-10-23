# Quotations

HTML has separate elements for a short quote inside a sentence and a longer quote set apart from the main text. It also has a way to name the source.

## Short quotes: `<q>`

Use `<q>` for a quotation inside a sentence:

```html
<p>Our teacher said, <q>Read the question twice before you answer it.</q></p>
```

Browsers usually add quotation marks. Do not type the quotes yourself as well.

## Block quotes: `<blockquote>`

Use `<blockquote>` for a longer quotation that stands on its own:

```html
<blockquote>
  <p>All animals are equal, but some animals are more equal than others.</p>
</blockquote>
```

A blockquote is a block element. Browsers usually indent it. If the quotation contains more than one paragraph, put each paragraph in its own `<p>` inside the blockquote.

## Naming the source

Use `<cite>` for the title of a work: a book, article, film, song, or report.

```html
<blockquote>
  <p>All animals are equal, but some animals are more equal than others.</p>
</blockquote>
<p>George Orwell, <cite>Animal Farm</cite></p>
```

`<cite>` is not for the author's name. The author goes in ordinary text; the title goes in `<cite>`.

The `cite` attribute on `<blockquote>` can hold a URL for the source, but it is not visible on the page:

```html
<blockquote cite="https://example.com/animal-farm">
  <p>All animals are equal, but some animals are more equal than others.</p>
</blockquote>
```

If readers need the source, add a visible link as well.

## Reference

| Element or attribute | Use for |
|----------------------|---------|
| `<q>` | A short inline quotation |
| `<blockquote>` | A longer quotation set apart from the text |
| `<cite>` | The title of a work |
| `cite` attribute | A URL for the source of a quotation |

## Exercise: quote a book

Find a sentence you like from a book, article, or speech. Add it to a page and include:

- a `<blockquote>` for the quotation,
- a visible source line,
- `<cite>` around the title of the work,
- a `cite` attribute if you have a URL for the source.

Check that the quotation marks appear once and that the source line names the work, not just the author.

Next: [Address and Fine Print](11-special-blocks.md)
