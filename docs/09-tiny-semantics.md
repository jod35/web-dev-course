# Tiny Semantics: Big Meaning

Some of the smallest tags do the most useful work. They don't change much visually, but they tell browsers, screen readers and search engines *what* your text actually is.

## Tag Reference

### `<abbr>`: Abbreviation

`<abbr>` marks an **abbreviation or acronym**. Pair it with `title` to give the full expansion:

```html
<p>I am learning <abbr title="HyperText Markup Language">HTML</abbr>.</p>
```

Browsers often show the `title` as a tooltip on hover, and assistive tech can use it too.

Another:

```html
<p>
    The <abbr title="World Health Organization">WHO</abbr>
    provides health information around the world.
</p>
```

---

### `<time>`: Date and Time

`<time>` flags a **specific date, time or period**.

```html
<p>The class starts at <time>9:00 AM</time>.</p>
```

For a date:

```html
<p>The event is on <time>2026-10-07</time>.</p>
```

Want to be machine-readable as well as human-friendly? Add `datetime`:

```html
<p>
    PyCon Africa starts on
    <time datetime="2026-10-07">October 7, 2026</time>.
</p>
```

Humans read "October 7, 2026"; computers parse `2026-10-07`.

---

### `<del>`: Deleted Text

`<del>` means text that's been **removed**:

```html
<p>
    The price is <del>50,000</del> 40,000 shillings.
</p>
```

Browsers usually strike it through.

---

### `<ins>`: Inserted Text

`<ins>` is the counterpart, text that's been **added**:

```html
<p>
    The price is <del>50,000</del> <ins>40,000</ins> shillings.
</p>
```

Useful when you're showing edits or price changes.

---

### `<sub>`: Subscript

`<sub>` sits **below the baseline**, think chemistry:

```html
<p>Water is H<sub>2</sub>O.</p>
```

Also handy for maths:

```html
<p>x<sub>1</sub> + x<sub>2</sub></p>
```

---

### `<sup>`: Superscript

`<sup>` sits **above the baseline**, exponents, ordinals:

```html
<p>2<sup>3</sup> = 8</p>
```

```html
<p>1<sup>st</sup> place</p>
```

---

## Summary

| Element  | What it means             |
| -------- | ------------------------- |
| `<abbr>` | Abbreviation or acronym   |
| `<time>` | Date or time              |
| `<del>`  | Deleted content           |
| `<ins>`  | Inserted content          |
| `<sub>`  | Subscript                 |
| `<sup>`  | Superscript               |

Tiny elements, but they add real semantic meaning, not just a visual tweak.
