# 06 - Combined: Headings + Paragraphs in the Basic Structure

**Goal:** In this chapter you will see where text lives inside the skeleton introduced in Chapter 01.

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

- The `<h1>` and `<p>` elements live **inside the `<body>` element**, because they are visible content.
- The `<head>` element holds **only** the `<title>` element in this example, and it never holds visible text, although the title itself appears on the browser tab.
- The `<html>` element is the **parent** of both sections, while `<!DOCTYPE html>` is the declaration above them all.


## Why this matters

- Text which is placed in `<head>` outside the `<title>` element **will not render**, and this mistake is a classic beginner bug.
- Every chapter from here on adds tags which live in `<body>`, except for page-level setup tags.

## Recap

| Zone | Holds | Visible? |
|------|-------|----------|
| `<head>` | `<title>`, `<meta>` | No, tab title only |
| `<body>` | `h1`–`h6`, `p`, and everything from Ch. 07 onward | Yes |

**Next:** [07 - Meaning vs Looks](07-meaning-vs-looks.md) · **Prev:** [05 - Paragraphs, Breaks, Rules](05-paragraphs-snippets.md)
