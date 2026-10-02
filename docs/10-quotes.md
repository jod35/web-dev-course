# 10 - Quotes

## 1. Inline Quotes

The `<q>` element is used for a **short quotation** within a sentence.

```html
<p>
    Albert Einstein said, <q>Imagination is more important than knowledge.</q>
</p>
```

Browsers normally display quotation marks around the text.

---

## 2. Block Quotes

The `<blockquote>` element is used for a **longer quotation** that stands on its own.

```html
<blockquote>
    The important thing is not to stop questioning.
    Curiosity has its own reason for existing.
</blockquote>
```

The browser normally displays a block quotation with indentation.

---

## 3. Citing the Source

The `cite` attribute can be used with `<blockquote>` to specify the source of a quotation.

```html
<blockquote cite="https://example.com/article">
    The important thing is not to stop questioning.
</blockquote>
```

The `cite` attribute provides the source information but is not normally displayed on the page.

---

## 4. The `<cite>` Element

The `<cite>` element is used to identify the **title of a work**, such as a book, movie, song, or article.

```html
<p>
    My favourite book is <cite>Things Fall Apart</cite>.
</p>
```

It can also be used when identifying the source of a quotation:

```html
<blockquote>
    The world is a fine place and worth fighting for.
</blockquote>

<p>
    Source: <cite>Ernest Hemingway</cite>
</p>
```

---

## 5. `<q>` vs `<blockquote>`

| Element          | Purpose                                  |
| ---------------- | ---------------------------------------- |
| `<q>`            | Short, inline quotation                  |
| `<blockquote>`   | Longer, separate quotation               |
| `<cite>`         | Identifies the title or source of a work |
| `cite` attribute | Specifies the URL of the source          |

### Example

```html
<p>
    She said, <q>Learning never stops.</q>
</p>

<blockquote>
    Education is the most powerful weapon which you can use
    to change the world.
</blockquote>
```
