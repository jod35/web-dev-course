# 16 - Forms Basics

**Goal:** collect user input with `form`, `label`, `input`, and `button`.

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
| `form` | Groups inputs; `action` = where data goes, `method` = `get` or `post` |
| `label` | Names an input,`for` must match the input's `id` |
| `input` | The field itself,`type` picks its behavior |
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
| `text` | Short text | Default type |
| `email` | Email address | Browser validates format |
| `number` | Number | `min`/`max`/`step` constrain |
| `date` | Calendar date | ISO value `YYYY-MM-DD` |
| `checkbox` | On/off | Label wrapping is fine |

`required` blocks empty submission; `name` is the key the server receives,an input without `name` sends nothing.

## Gotchas

- Clicking a `<label>` focuses its input,if it doesn't, your `for`/`id` mismatch.
- `method="get"` puts data in the URL (searchable/shareable); `post` hides it in the request (orders, logins).
- Never trust browser validation alone,servers must re-check everything.

## Recap

| Rule | Detail |
|------|--------|
| Label everything | `for` ↔ `id`, always |
| Name everything | No `name` = no data sent |
| Submit | `<button type="submit">`, not a link |

**Next:** [17,Grouping](17-div-section.md) · **Prev:** [15,Tables](15-tables.md)
