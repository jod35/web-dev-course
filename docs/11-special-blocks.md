# Address and Fine Print

Two small elements often appear near the end of a page: `<address>` for contact information and `<small>` for secondary text.

## `<address>`: contact information

Use `<address>` for contact information for the author or owner of the page or section. It is not for any postal address that happens to appear in the content.

```html
<address>
  MHSM Web Club<br>
  Makerere High School Migadde<br>
  <a href="mailto:webclub@example.com">webclub@example.com</a>
</address>
```

`<address>` is a block element. Browsers usually show it in italics. Contact information often belongs in a page footer:

```html
<footer>
  <p>Questions? Contact the web club.</p>
  <address>
    <a href="mailto:webclub@example.com">webclub@example.com</a>
  </address>
</footer>
```

Do not use `<address>` for a shop's delivery address, a venue address, or a random location in the content. Use a normal paragraph for those.

## `<small>`: fine print

Use `<small>` for side comments, copyright notices, disclaimers, and attribution:

```html
<p><small>Prices include tax and are valid until the end of the term.</small></p>
```

Browsers display it a little smaller than normal text. That does not make the content unimportant. It means the content is secondary:

```html
<footer>
  <p><small>&copy; 2026 MHSM Web Club. All rights reserved.</small></p>
</footer>
```

Do not use `<small>` to hide important information, and do not use it just because you want smaller text. Use CSS for styling.

## Reference

| Element | Use for | Avoid |
|---------|---------|-------|
| `<address>` | Contact details for the page or section author | Any postal address in the content |
| `<small>` | Copyright, disclaimers, attribution | Hiding important information |

## Exercise: add a footer

Add a footer to a page you have already built. Include:

- one sentence about who made the page,
- an `<address>` with an email link,
- a `<small>` copyright line with the current year.

Check that the email link uses `mailto:` and that the address is contact information, not a location mentioned in the page content.

Next: [Links](12-links.md)
