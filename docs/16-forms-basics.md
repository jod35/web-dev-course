# Forms

Forms collect information from the reader: a login, a search, a registration, or a message. A form is a set of controls inside a `<form>` element.

```html
<form>
  <p>
    <label for="name">Name</label>
    <input type="text" id="name" name="name">
  </p>
  <button type="submit">Submit</button>
</form>
```

The form above has a label, a text field, and a submit button. It does not send the data anywhere yet because the `action` is missing.

## Labels

Every input needs a label. Use `<label for="...">` and match it to the input's `id`:

```html
<label for="email">Email</label>
<input type="email" id="email" name="email">
```

The `for` value must match the `id` exactly. Clicking the label then focuses the input, and screen readers can announce which field is which.

Do not replace a label with a placeholder. Placeholders disappear as soon as the reader types.

## Input types

The `type` attribute changes what the input accepts and which keyboard appears on mobile:

| Type | Use for |
|------|---------|
| `text` | General single-line text |
| `email` | Email addresses |
| `password` | Passwords, hidden as typed |
| `number` | Numbers |
| `date` | A date |
| `time` | A time |
| `search` | Search terms |
| `checkbox` | Several choices |
| `radio` | One choice from a group |
| `file` | Uploading a file |
| `submit` | A submit button |

```html
<label for="age">Age</label>
<input type="number" id="age" name="age" min="10" max="100">
```

Browsers can validate some types. An `email` input rejects text that does not look like an email address, and `required` blocks an empty submission.

## Longer text: `<textarea>`

Use `<textarea>` for multiple lines:

```html
<label for="message">Message</label>
<textarea id="message" name="message" rows="5"></textarea>
```

The `rows` attribute sets the visible height. It is a starting size, not a character limit.

## Drop-down lists: `<select>` and `<option>`

```html
<label for="country">Country</label>
<select id="country" name="country">
  <option value="uganda">Uganda</option>
  <option value="kenya">Kenya</option>
  <option value="tanzania">Tanzania</option>
</select>
```

Each `<option>` is one choice. The `value` is what gets submitted.

## Radio buttons: one choice

Radio buttons in the same group share a `name`. Only one can be selected.

```html
<fieldset>
  <legend>Year of study</legend>

  <label>
    <input type="radio" name="year" value="s1">
    S1
  </label>

  <label>
    <input type="radio" name="year" value="s2">
    S2
  </label>
</fieldset>
```

`<fieldset>` groups related controls. `<legend>` gives the group a name. This is much clearer than putting the question in a separate paragraph.

## Checkboxes: several choices

Checkboxes use the same `name` when they belong to one question, but each can be selected independently:

```html
<fieldset>
  <legend>Languages you know</legend>

  <label>
    <input type="checkbox" name="language" value="python">
    Python
  </label>

  <label>
    <input type="checkbox" name="language" value="javascript">
    JavaScript
  </label>
</fieldset>
```

## `name` and `value`

- `id` identifies the element within the page. It connects a label to its control.
- `name` identifies the field when the form is submitted.
- `value` is the data sent for that control.

```html
<label for="username">Username</label>
<input type="text" id="username" name="username">
```

If a field has no `name`, its value is not submitted.

## Required fields and placeholders

```html
<label for="email">Email</label>
<input
  type="email"
  id="email"
  name="email"
  placeholder="you@example.com"
  required
>
```

`required` makes the field mandatory. `placeholder` shows a temporary hint inside the field. Use a placeholder for an example format, not as a replacement for a label.

## Submitting the form

A submit button sends the form:

```html
<button type="submit">Register</button>
```

Use `type="button"` for a button that should not submit the form.

The `action` attribute says where the data goes, and `method` says how:

```html
<form action="/register" method="post">
```

- `GET` puts the values in the URL. It is suitable for searches and requests that do not change data.
- `POST` sends the values in the request body. It is suitable for registrations, logins, and other changes.

You will need a server to process the data. For now, focus on the markup and the browser's built-in validation.

## A complete registration form

```html
<form action="/register" method="post">
  <h2>Create an account</h2>

  <p>
    <label for="name">Name</label>
    <input type="text" id="name" name="name" required>
  </p>

  <p>
    <label for="email">Email</label>
    <input type="email" id="email" name="email" required>
  </p>

  <p>
    <label for="password">Password</label>
    <input type="password" id="password" name="password" required>
  </p>

  <fieldset>
    <legend>Year of study</legend>
    <label>
      <input type="radio" name="year" value="s1">
      S1
    </label>
    <label>
      <input type="radio" name="year" value="s2">
      S2
    </label>
  </fieldset>

  <p>
    <label for="country">Country</label>
    <select id="country" name="country">
      <option value="uganda">Uganda</option>
      <option value="kenya">Kenya</option>
      <option value="tanzania">Tanzania</option>
    </select>
  </p>

  <p>
    <label for="message">About you</label>
    <textarea id="message" name="message" rows="4"></textarea>
  </p>

  <button type="submit">Register</button>
</form>
```

The fields are wrapped in paragraphs so they appear on separate lines. CSS can arrange them in columns later.

## Check your work

- Does every input have a label?
- Does every label's `for` match an input `id`?
- Do radio buttons in one group share a `name`?
- Are radio buttons and checkboxes inside a `<fieldset>` with a `<legend>`?
- Does every control that should be submitted have a `name`?
- Did you use `required` only on fields that are genuinely required?
- Does the form still make sense when navigated with the Tab key?

## Try it

Build a contact form with:

1. a name field,
2. an email field,
3. a drop-down for the reason for contact,
4. a radio group for preferred contact method,
5. a message textarea,
6. a submit button.

Open the form and try to submit it while the required fields are empty. Read the browser's message. Then fill it in and check that the fields accept the expected input.

Next: [Grouping Content](17-div-section.md)
