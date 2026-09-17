# 11,Special Blocks

**Goal:** three block tags for exact whitespace, contact info, and fine print.

## Tag reference

### `<pre>`,preformatted text

Keeps **spaces and line breaks exactly** as typed,the only element that does. The home of multi-line code:

```html
<pre>line 1
  indented line 2</pre>
```

Pair with `<code>` for code blocks with meaning:

```html
<pre><code>def hello():
    print("hi")</code></pre>
```

### `<address>`,contact info

Contact information for the **page/section author or owner**,not any postal address found in text:

```html
<address>hello@mhsm.web<br>Dar es Salaam</address>
```

Browsers usually italicize it. It belongs near the footer or author bio.

### `<small>`,fine print

Side comments: copyright, disclaimers, legal notes, attributions:

```html
<small>© 2026 MHSM. All rights reserved.</small>
```

Browsers render it one step smaller. It does **not** make text unimportant,only secondary.

## Gotchas

- Inside `<pre>`, you must still escape `<` as `&lt;` or the browser reads it as a tag.
- `<address>` must not contain headings or sectioning content,only contact lines.
- `<small>` inside `<footer>` is the classic copyright pattern.

## Recap

| Tag | Job | Watch out |
|-----|-----|-----------|
| `pre` | Exact whitespace | Escape `<` as `&lt;` |
| `address` | Author/owner contact | Not any address |
| `small` | Fine print | Still readable, not hidden |

**Next:** [12,Links](12-links.md) · **Prev:** [10,Quotes](10-quotes.md)
