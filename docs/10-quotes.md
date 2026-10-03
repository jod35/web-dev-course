# Quotes

HTML makes a useful distinction between a quick quote inside a sentence and a longer passage set apart. It also gives you a clean way to say *where* a quote came from.

## 1. Inline Quotes

`<q>` is for a **short quotation inside a sentence**:

```html
<p>
    Albert Einstein said, <q>Imagination is more important than knowledge.</q>
</p>
```

Browsers typically wrap it in quotation marks for you, no need to type them by hand.

---

## 2. Block Quotes

For a **longer quotation that stands on its own**, use `<blockquote>`:

```html
<blockquote>
    The important thing is not to stop questioning.
    Curiosity has its own reason for existing.
</blockquote>
```

Browsers usually indent block quotes to set them apart.

---

## 3. Citing the Source

You can attach a source URL directly to `<blockquote>` with `cite`:

```html
<blockquote cite="https://example.com/article">
    The important thing is not to stop questioning.
</blockquote>
```

That `cite` attribute won't be visible on the page, but it's there for tools that want it.

---

## 4. The `<cite>` Element

`<cite>` identifies the **title of a work**, a book, film, song, article:

```html
<p>
    My favourite book is <cite>Things Fall Apart</cite>.
</p>
```

You can use it for attributions too:

```html
<blockquote>
    The world is a fine place and worth fighting for.
</blockquote>

<p>
    Source: <cite>Ernest Hemingway</cite>
</p>
```

---

## 5. `<q>` vs `<blockquote>`: Which One?

| Element / Attribute | Purpose |
| ------------------- | ------- |
| `<q>` | Short, inline quotation |
| `<blockquote>` | Longer, standalone quotation |
| `<cite>` | Title or source of a work |
| `cite` attribute | URL of the source |

Example with both:

```html
<p>
    She said, <q>Learning never stops.</q>
</p>

<blockquote>
    Education is the most powerful weapon which you can use
    to change the world.
</blockquote>
```
