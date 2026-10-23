# Small Semantic Tags

Some useful HTML elements do not change the page much. Their job is to add meaning that browsers and screen readers can use.

## Abbreviations: `<abbr>`

Use `<abbr>` for an abbreviation or acronym. The `title` attribute gives the full form:

```html
<p>I am learning <abbr title="HyperText Markup Language">HTML</abbr>.</p>
```

The full form may appear as a tooltip when the reader hovers over the abbreviation. Do not use `title` to repeat information that is already visible.

## Dates and times: `<time>`

`<time>` marks a specific date, time, or duration:

```html
<p>Sports Day starts at <time datetime="08:00">8am</time>.</p>
<p>The event is on <time datetime="2026-11-06">Friday, 6 November</time>.</p>
```

The text between the tags is for humans. The `datetime` attribute is machine-readable. It uses the format `YYYY-MM-DD` for dates and `HH:MM` for times.

You can also mark a duration:

```html
<p>The journey takes <time datetime="PT2H30M">two and a half hours</time>.</p>
```

## Deleted and inserted text: `<del>` and `<ins>`

Use `<del>` for text that has been removed and `<ins>` for text that has been added:

```html
<p>The price is <del>5,000</del> <ins>4,000</ins> shillings.</p>
```

Browsers usually show `<del>` with a line through it and `<ins>` underlined. This is useful for price changes, corrections, and showing edits. Add `datetime` if the time of the change matters.

## Subscript and superscript

`<sub>` lowers text below the baseline. `<sup>` raises it above the baseline.

```html
<p>Water is H<sub>2</sub>O.</p>
<p>2<sup>3</sup> = 8.</p>
```

Do not use these elements just to move text around visually. Use CSS for positioning.

## Reference

| Element | Meaning | Example |
|---------|---------|---------|
| `<abbr>` | Abbreviation or acronym | `<abbr title="World Health Organization">WHO</abbr>` |
| `<time>` | Date, time, or duration | `<time datetime="2026-11-06">6 November</time>` |
| `<del>` | Removed text | `<del>5,000</del>` |
| `<ins>` | Inserted text | `<ins>4,000</ins>` |
| `<sub>` | Subscript | `H<sub>2</sub>O` |
| `<sup>` | Superscript | `2<sup>3</sup>` |

## Exercise: update a notice

Take this notice and add the appropriate semantic tags:

```html
<p>The WHO visit is on 6 November.</p>
<p>The meeting starts at 9am.</p>
<p>The old venue was the library. The new venue is the school hall.</p>
<p>The price of lunch is 5,000 shillings.</p>
<p>Water is H2O.</p>
```

Check that:

- the abbreviation has a full form,
- both dates and times use `<time>`,
- the old and new information use `<del>` and `<ins>`,
- the chemical formula uses `<sub>`.

Next: [Quotations](10-quotes.md)
