# 11 - Special Blocks

**Goal:** In this chapter you will learn three block tags for exact whitespace, contact information, and fine print.

## Tag reference

### `<pre>` - preformatted text

The `pre` element keeps **spaces and line breaks exactly** as you type them, and it is the only element which behaves this way. It is the home of multi-line code:

```html
<pre>line 1
  indented line 2</pre>
```

Pair the `pre` element with the `<code>` element when you want a code block which also carries meaning:

```html
<pre><code>def hello():
    print("hi")</code></pre>
```

### `<address>` - contact info

The `address` element holds contact information for the **author or owner of the page or section**, and it must not be used for any postal address which happens to appear in the text:

```html
<address>hello@mhsm.web<br>Dar es Salaam</address>
```

Browsers usually render this element in italic. It belongs near the footer or the author bio.

### `<small>` - fine print

The `small` element holds side comments such as copyright lines, disclaimers, legal notes, and attributions:

```html
<small>© 2026 MHSM. All rights reserved.</small>
```

Browsers render it one step smaller than normal text. It does **not** make the text unimportant, since it only marks the text as secondary.

## Rules

- Inside a `<pre>` element, you must still escape `<` as `&lt;`, because otherwise the browser reads it as a tag.
- The `<address>` element must not contain headings or sectioning content, so restrict it to contact lines.
- A `<small>` element inside a `<footer>` element is the classic pattern for a copyright line.

## Recap

| Tag | Job | Watch out |
|-----|-----|-----------|
| `pre` | Exact whitespace | Escape `<` as `&lt;` |
| `address` | Author or owner contact | Not any address |
| `small` | Fine print | Still readable, not hidden |

**Next:** [12 - Links](12-links.md) · **Prev:** [10 - Quotes](10-quotes.md)
