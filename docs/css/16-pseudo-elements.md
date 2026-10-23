# Pseudo-elements

A pseudo-element styles a part of an element or generates content that is not in the HTML. Pseudo-elements use a double colon: `::before`.

## Common pseudo-elements

```css
p::first-line {
  font-weight: 600;
}

p::first-letter {
  font-size: 1.5rem;
}

::selection {
  background: #0a58ca;
  color: #fff;
}

input::placeholder {
  color: #6b7280;
}
```

- `::first-line` styles the first line of a block.
- `::first-letter` styles the first letter.
- `::selection` styles selected text.
- `::placeholder` styles a form placeholder.

## Generated content

`::before` and `::after` need a `content` value:

```css
blockquote::before {
  content: "“";
  color: #999;
}

.badge::after {
  content: " new";
  font-size: 0.875em;
  color: crimson;
}
```

They behave like the first and last child of the element. Use them for decoration, not for content that belongs in the HTML. Text added with `content` may not be announced consistently by screen readers, and it cannot be selected or copied like normal content.

## A visual accent

```css
.card::before {
  content: "";
  display: block;
  height: 4px;
  background: var(--primary, #0a58ca);
}
```

An empty `content` value creates a decorative box. This is acceptable when the decoration does not carry meaning.

## Single or double colon?

Modern syntax uses `::before`, `::after`, `::first-line`, and `::first-letter`. The single-colon forms for `:before` and `:after` still work in browsers, but prefer the double colon.

## Try it

1. Add a decorative accent to a card with `::before`.
2. Use `::first-letter` on the first paragraph of an article.
3. Change the selection colour with `::selection`.
4. Add `::after` content to a badge, then disable it and check that no important information is lost.
5. Remove any generated content that a reader would need in order to understand the page.

If generated content appears in the wrong place, check the element's `display` value and whether it is positioned.

Next: [Pseudo-classes](17-pseudo-classes.md)
