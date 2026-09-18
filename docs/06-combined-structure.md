# 06 - Combined: Headings + Paragraphs in the Basic Structure

**Goal:** see where text lives inside the skeleton from Chapter 01.

## The same skeleton - now with text

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bakery</title>
</head>
<body>
  <h1>Bakery</h1>
  <p>Fresh bread daily.</p>
</body>
</html>
```

## Where each piece lives

- `<h1>` and `<p>` live **inside `<body>`**,they are visible content.
- `<head>` holds **only** `<title>` here, never visible text (the title shows on the browser tab).
- `<html>` is the **parent** of both; `<!DOCTYPE html>` is the declaration above it all.


## Why this matters

- Text placed in `<head>` (outside `<title>`) **will not render**,a classic beginner bug.
- Every chapter from here on adds tags that live in `<body>`, except page-level setup.

## Recap

| Zone | Holds | Visible? |
|------|-------|----------|
| `<head>` | `<title>`, `<meta>` | No (tab title only) |
| `<body>` | `h1`–`h6`, `p`, everything in Ch. 07+ | Yes |

**Next:** [07 - Meaning vs Looks](07-meaning-vs-looks.md) · **Prev:** [05 - Paragraphs, Breaks, Rules](05-paragraphs-snippets.md)
