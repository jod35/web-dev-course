# 01 - Basic Structure of an HTML Page

**Goal:** In this chapter you will learn the skeleton on which every webpage is built, starting with the declaration, then the single root element, then the metadata, and finally the visible content.

## The full template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Your Page Title</title>
</head>
<body>
  <!-- Your page content -->
</body>
</html>
```

Copy this template at the start of **every** page. Read it from top to bottom, because the order is significant.

## Tag reference

### `<!DOCTYPE html>` - declaration

- This line declares the document as **HTML5** so that browsers render the page in standards mode instead of quirks mode.
- It is **not a tag**, so it has no closing tag and no attributes. It must always be the very first line, with nothing above it.

```html
<!DOCTYPE html>
```

### `<html>` - root element

- The `html` element is the **parent of everything**. It wraps both `<head>` and `<body>`, and its closing tag `</html>` must be the last line of the file.
- The `lang` attribute sets the page language, which **screen readers and search engines use**:

```html
<html lang="en">
```

| `lang` value | Meaning |
|--------------|---------|
| `en` | English |
| `sw` | Swahili |
| `fr` | French |

### `<head>` - invisible metadata

- The `head` element holds setup information which the visitor **never sees on the page itself**, including `<title>`, `<meta charset>`, `<meta viewport>`, `<link>` to CSS, and `<script>` to JS.
- It is the first child of `<html>`, and it always appears **before** `<body>`.

```html
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Bakery</title>
</head>
```

| Tag inside `<head>` | Job |
|---------------------|-----|
| `<title>` | The tab and window title, which is also used as the search-result title |
| `<meta charset="utf-8">` | The character encoding, which should always be included |
| `<meta name="viewport" …>` | The instruction which makes mobile browsers scale the page correctly, and which should always be included |

### `<body>` - visible content

- **Everything the visitor sees** belongs in the body, including headings, paragraphs, lists, images, links, and divs.
- It is the second child of `<html>`, and each page contains exactly **one** `<body>` element.

```html
<body>
  <h1>Bakery</h1>
  <p>Fresh bread daily.</p>
</body>
```

<figure markdown="span">
![The struture of an HTML page](./imgs/structure.png)
<figcaption> The struture of an HTML page </figcaption>
</figure>

## Hierarchy (who is inside who)

```text
<!DOCTYPE html>      declaration,comes first, owns nothing
<html>               PARENT,wraps all
  <head>             1st child,invisible setup
  <body>             2nd child,all visible content
```

- The `<html>` element is the **parent**, while `<head>` and `<body>` are its **children**.
- The `<head>` element always appears **before** the `<body>` element. No visible content ever belongs in `<head>`, although the `<title>` appears on the browser tab.

## Rules

- Each page contains one `<!DOCTYPE>`, one `<html>`, one `<head>`, and one `<body>`, with no additional copies.
- Close the tags in reverse order, so the `<html>` tag which opens second also closes last.
- If you omit `<meta charset>`, non-English characters can display incorrectly. If you omit the viewport tag, the layout breaks on mobile phones.

## Recap

| Order | Tag | Role |
|-------|-----|------|
| 1st | `<!DOCTYPE html>` | Declaration |
| 2nd | `<html lang>` | Root parent |
| 3rd | `<head>` | Invisible metadata |
| 4th | `<body>` | Visible content |

**Next:** [02 - What Are Headings?](02-headings.md)
