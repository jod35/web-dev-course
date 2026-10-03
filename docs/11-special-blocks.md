# Special Blocks

Three block tags you'll use less often, but when you need them, nothing else will do: one for exact whitespace, one for contact info, and one for fine print.

## Tag reference

### `<pre>` — preformatted text

`pre` is the only element that keeps **spaces and line breaks exactly** as you type them. That's why it's the home for multi-line code:

```html
<pre>line 1
  indented line 2</pre>
```

If you want a code block that also says "this is code," pair it with `<code>`:

```html
<pre><code>def hello():
    print("hi")</code></pre>
```

### `<address>` — contact info

`address` holds contact information for the **author or owner of the page or section** — not just any postal address that happens to appear in your text:

```html
<address>hello@mhsm.web<br>Dar es Salaam</address>
```

Browsers usually italicise it. You'll typically see it near the footer or an author bio.

### `<small>` — fine print

`small` is for side comments — copyright, disclaimers, legal notes, attributions:

```html
<small>© 2026 MHSM. All rights reserved.</small>
```

Browsers render it a touch smaller than normal text. It doesn't make the text unimportant — it just marks it as secondary.

## A few things to watch

- Inside `<pre>` you still need to escape `<` as `&lt;` — otherwise the browser thinks it's a tag.
- `<address>` shouldn't contain headings or sectioning content — keep it to contact lines.
- `<small>` inside `<footer>` is the classic combo for a copyright line.

## Recap

| Tag | Job | Watch out |
|-----|-----|-----------|
| `pre` | Exact whitespace | Escape `<` as `&lt;` |
| `address` | Author/owner contact | Not any random address |
| `small` | Fine print | Still readable, not hidden |
