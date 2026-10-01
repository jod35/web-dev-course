# 09 - Tiny Semantics - Big Meaning

### Goal

In this chapter, you will learn about small HTML elements that add **meaning** to text. These elements help browsers, search engines, screen readers, and other tools understand what the content represents.

## Tag Reference

### `<abbr>` - Abbreviation

The `<abbr>` element represents an **abbreviation or acronym**.

```html
<p>I am learning <abbr title="HyperText Markup Language">HTML</abbr>.</p>
```

The `title` attribute provides the full meaning of the abbreviation.

When the user hovers over the abbreviation, browsers commonly display the value of `title`.

Another example:

```html
<p>
    The <abbr title="World Health Organization">WHO</abbr>
    provides health information around the world.
</p>
```

---

### `<time>` - Date and Time

The `<time>` element represents a **specific date, time, or period**.

```html
<p>The class starts at <time>9:00 AM</time>.</p>
```

For a date:

```html
<p>The event is on <time>2026-10-07</time>.</p>
```

The `datetime` attribute can provide a machine-readable version of the date or time.

```html
<p>
    PyCon Africa starts on
    <time datetime="2026-10-07">October 7, 2026</time>.
</p>
```

The text is written for humans, while `datetime` gives computers a standard format to understand.

---

### `<del>` - Deleted Text

The `<del>` element represents text that has been **removed or deleted**.

```html
<p>
    The price is <del>50,000</del> 40,000 shillings.
</p>
```

Browsers normally display deleted text with a line through it.

---

### `<ins>` - Inserted Text

The `<ins>` element represents text that has been **added or inserted**.

```html
<p>
    The price is <del>50,000</del> <ins>40,000</ins> shillings.
</p>
```

This can be useful when showing changes to a document.

---

### `<sub>` - Subscript

The `<sub>` element displays text **below the normal text line**.

It is commonly used in chemical formulas.

```html
<p>Water is H<sub>2</sub>O.</p>
```

It can also be used in mathematical expressions:

```html
<p>x<sub>1</sub> + x<sub>2</sub></p>
```

---

### `<sup>` - Superscript

The `<sup>` element displays text **above the normal text line**.

It is commonly used for powers and mathematical expressions.

```html
<p>2<sup>3</sup> = 8</p>
```

It can also be used for ordinal numbers:

```html
<p>1<sup>st</sup> place</p>
```

---

## Summary

| Element  | Meaning                 |
| -------- | ----------------------- |
| `<abbr>` | Abbreviation or acronym |
| `<time>` | Date or time            |
| `<del>`  | Deleted content         |
| `<ins>`  | Inserted content        |
| `<sub>`  | Subscript               |
| `<sup>`  | Superscript             |

These elements may look small, but they give HTML **semantic meaning** rather than simply changing how text looks.

**Next:** [10 - Quotes](10-quotes.md) · **Prev:** [08 - Code Family](08-code-family.md)
