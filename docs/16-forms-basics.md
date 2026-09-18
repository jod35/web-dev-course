# 16 - Forms Basics

**Goal:** In this chapter you will learn how to collect user input with `form`, `label`, `input`, and `button`.

## Minimal form

```html
<form action="/order" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  <button type="submit">Order</button>
</form>
```

| Piece | Job |
|-------|-----|
| `form` | Groups inputs, where `action` states where the data goes and `method` is either `get` or `post` |
| `label` | Names an input, where `for` must match the input's `id` |
| `input` | The field itself, where `type` selects its behaviour |
| `button type="submit"` | Sends the form |

## Common `input` types

```html
<label for="mail">Email:</label>
<input type="email" id="mail" name="mail" required>

<label for="qty">Loaves:</label>
<input type="number" id="qty" name="qty" min="1" max="12" value="1">

<label for="day">Pickup day:</label>
<input type="date" id="day" name="day">

<label for="note">Note:</label>
<textarea id="note" name="note" rows="3"></textarea>

<label><input type="checkbox" name="sliced"> Sliced</label>
```

| `type` | Collects | Notes |
|--------|----------|-------|
| `text` | Short text | The default type |
| `email` | Email address | The browser validates the format |
| `number` | Number | `min`, `max`, and `step` constrain the value |
| `date` | Calendar date | The value uses ISO format `YYYY-MM-DD` |
| `checkbox` | On or off state | Wrapping the input in a label is acceptable |

The `required` attribute blocks empty submission, while the `name` attribute is the key which the server receives, so an input without a `name` attribute sends nothing.

## Rules

- When you click a `<label>` element, the browser focuses its input. If that focus does not happen, your `for` and `id` values do not match.
- The value `method="get"` places the data in the URL, which makes it searchable and shareable, while `post` hides the data in the request, which suits orders and logins.
- Never trust browser validation alone, because the server must re-check everything.

## Recap

| Rule | Detail |
|------|--------|
| Label everything | Always pair `for` with `id` |
| Name everything | Without a `name` attribute, no data is sent |
| Submit | Use `<button type="submit">` instead of a link |

**Next:** [17 - Grouping](17-div-section.md) · **Prev:** [15 - Tables](15-tables.md)
