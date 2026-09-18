# 04 - What Are Paragraphs?

**Goal:** In this chapter you will learn how paragraphs work as blocks of thought, and how `br` and `hr` differ from paragraphs.

## Paragraphs = blocks of thought

A paragraph groups sentences into **one block which expresses one idea**. It is the default unit of web text:

```html
<p>Fresh bread baked every morning.</p>
```

- **Block-level:** Each `<p>` element starts on a new line, and browsers add space above and below it automatically.
- **Readability:** Each `<p>` element should hold one idea. Short paragraphs scan far better on screens than long walls of text.

## `<p>` vs `<br>`

- The `<p>` element starts a **new thought**, which means it creates a new block.
- The `<br>` element creates a line break **inside the same thought**, which is useful for an address, a poem, or a signature block:

```html
<p>Line one<br>Line two, same thought</p>
```

<figure markdown="span">

![Image title](./imgs/paragraphs.png){ width="400" }

<figcaption>Paragraphs</figcaption>

</figure>



**Never** stack several `<br>` tags such as `<br><br><br>` in order to fake paragraph spacing. The `<p>` element, together with CSS margins, exists for that purpose, while stacked breaks carry no meaning for screen readers.

## `<hr>` = thematic break

The `<hr>` element marks a **scene change** between blocks, for example when a story moves to a new scene or when a menu switches to prices:

```html
<p>Menu</p>
<hr>
<p>Prices</p>
```

It renders as a horizontal line, but its meaning is that the topic shifts at this point, so it is **not** decoration.

## Rules

1. Place one idea in each `<p>` element and keep paragraphs short.
2. The `<br>` element is an empty tag without a closing tag, and it should be used sparingly.
3. The `<hr>` element is an empty tag which signals a shift in topic, not a decorative divider.

## Recap

| Tag | Meaning | Empty? |
|-----|---------|--------|
| `p` | Block of thought | No |
| `br` | Line break within the same thought | Yes |
| `hr` | Thematic break | Yes |

**Next:** [05 - Paragraphs, Breaks, Rules](05-paragraphs-snippets.md) · **Prev:** [03 - Headings h1–h6](03-headings-showcase.md)
