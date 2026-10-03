# Pseudo-elements

Pseudo-elements style a *part* of an element, or generate content that is not in your HTML.

They use `::` double colon.

## Common ones

```css
p::first-line { font-weight: 600; }
p::first-letter { font-size: 1.5rem; }
::selection { background: #0a58ca; color: #fff; }
```

## Generated content

`::before` and `::after` need `content`, then they behave like a child element:

```css
blockquote::before { content: "“"; color: #999; }
.badge::after { content: " new"; font-size: 0.875em; color: crimson; }
```

```html
<blockquote>Learning never stops.</blockquote>
```

Do not use `::before`/`::after` for real content that should be in HTML. Use them for decoration.

## Styling form controls

```css
input::placeholder { color: #6b7280; }
```

## Example: custom marker

```css
.card::before {
  content: "";
  display: block;
  height: 4px;
  background: var(--primary, #0a58ca);
  border-radius: 999px;
}
```

## Single vs double colon

Modern syntax is `::before`, `::after`, `::first-line`. Old single colon `:before` still works for the first two, but prefer `::`.

## Recap

| Pseudo-element | Role |
|----------------|------|
| `::before`, `::after` | Generated content, needs `content` |
| `::first-line`, `::first-letter` | Part of text |
| `::selection` | Selected text |
| `::placeholder` | Placeholder text |
