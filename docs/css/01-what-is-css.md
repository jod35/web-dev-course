# What is CSS?

HTML says what things are. CSS says how they look. A paragraph stays a paragraph, but CSS decides its color, size, spacing, and where it sits on the page.

## A first rule

```css
p {
  color: #333;
  line-height: 1.6;
}
```

Read it as: select `p` elements, then apply these declarations.

```text
p          → selector (what to style)
{ }        → declaration block
color      → property
#333       → value
```

Another:

```css
h1 {
  font-size: 2rem;
  margin-bottom: 0.5rem;
}
```

## Where CSS lives

**External file (use this by default):**

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

```css
/* styles.css */
body {
  font-family: system-ui, sans-serif;
}
```

**Internal (in `<style>`) — handy for quick tests:**

```html
<style>
  p { color: crimson; }
</style>
```

**Inline (avoid for normal styling):**

```html
<p style="color: crimson;">Hello</p>
```

Prefer external files. They keep HTML readable, let browsers cache the CSS, and let you style many pages from one place.

## The shape to remember

```css
selector {
  property: value;
  property: value;
}
```

Example with two declarations:

```css
.card {
  padding: 1rem;
  border: 1px solid #ddd;
}
```

If you can read that shape, you can read any CSS file.

## A small habit

Start every CSS project with this at the top of `styles.css`:

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
  color: #222;
}
```

It normalizes sizing and gives you a clean, readable baseline. You will tweak it later, but starting here saves surprises.

## Recap

| Question | Answer |
|----------|--------|
| What does CSS do? | Controls presentation of HTML |
| Where should it live? | In an external `styles.css` linked from `<head>` |
| What is a rule? | Selector plus declaration block |

Next: selectors — how to target exactly the elements you want.
