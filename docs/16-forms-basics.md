# Forms Basics

Forms are how users **give you information** — log in, register, search, give feedback, place an order. If a page needs input, you'll likely need a form.

## What is a Form?

It's simply a section of a page where people can **enter or pick information**. You'll see them for logins, registrations, contact pages, search boxes, surveys and bookings.

A tiny example:

```html
<form>
    <label for="name">Name:</label>
    <input type="text" id="name">

    <button type="submit">Submit</button>
</form>
```

---

# `<form>` — The Container

`<form>` wraps the controls that collect information:

```html
<form>

    <!-- Form controls go here -->

</form>
```

Inside you can place things like `<input>`, `<label>`, `<textarea>`, `<select>`, `<button>`, `<fieldset>` and friends.

---

# `<label>` — Describing a Control

`<label>` tells users what a field is for. Link it to the input via `for` ↔ `id`:

```html
<label for="name">Name:</label>
<input type="text" id="name">
```

```text
for="name"
     ↓
id="name"
```

That connection also means clicking the label focuses the input — a small usability win.

---

# `<input>` — The Workhorse

`<input>` can collect many kinds of data. The `type` attribute says which:

```html
<input type="text">
```

Common types:

| Type | When you'd use it |
| ---- | ----------------- |
| `text` | General text |
| `email` | Email address (browser can validate) |
| `password` | Password (hidden as you type) |
| `number` | Numeric value |
| `date` | Pick a date |
| `time` | Pick a time |
| `checkbox` | Multiple choices |
| `radio` | One choice from a group |
| `file` | File upload |
| `search` | Search box |
| `submit` | Submit the form |

---

# Text Input

```html
<label for="name">Name:</label>
<input type="text" id="name">
```

A user might type:

```text
Jonathan
```

---

# Email Input

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

Browsers can then validate the shape of an email and show a suitable keyboard on mobile.

---

# Password Input

```html
<label for="password">Password:</label>
<input type="password" id="password">
```

Characters are hidden as you type — as you'd expect.

---

# Number Input

```html
<label for="age">Age:</label>
<input type="number" id="age">
```

You can bound it:

```html
<input type="number" id="age" min="10" max="100">
```

---

# Date Input

```html
<label for="birthday">Date of Birth:</label>
<input type="date" id="birthday">
```

The browser will often show a date picker.

---

# Time Input

```html
<label for="appointment">Appointment Time:</label>
<input type="time" id="appointment">
```

---

# Textarea — For Longer Text

When you need **multiple lines**, use `<textarea>` — unlike `<input>`, it has an opening and closing tag:

```html
<label for="message">Message:</label>

<textarea id="message"></textarea>
```

Size it with `rows`/`cols` if you like:

```html
<textarea id="message" rows="5" cols="40"></textarea>
```

---

# Select and Option — Drop-Down

`<select>` creates the list; `<option>`s are the choices:

```html
<label for="country">Country:</label>

<select id="country">
    <option>Uganda</option>
    <option>Kenya</option>
    <option>Tanzania</option>
    <option>Rwanda</option>
</select>
```

---

# Radio Buttons — Pick One

Radios let you choose **one option from a group**. The key is they share the same `name`:

```html
<p>Gender:</p>

<input type="radio" id="male" name="gender" value="male">
<label for="male">Male</label>

<input type="radio" id="female" name="gender" value="female">
<label for="female">Female</label>
```

```html
name="gender"
```
→ tells the browser they belong together.

---

# Checkboxes — Pick Many

Unlike radios, you can tick **several** boxes:

```html
<p>Languages you know:</p>

<input type="checkbox" id="python" name="language" value="python">
<label for="python">Python</label>

<input type="checkbox" id="javascript" name="language" value="javascript">
<label for="javascript">JavaScript</label>

<input type="checkbox" id="java" name="language" value="java">
<label for="java">Java</label>
```

---

# The `name` Attribute

`name` is what the form sends to the server:

```html
<input type="text" name="username">
```

Example with both:

```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

* `id` — identifies the element *in the page* (for `<label>`).
* `name` — identifies the field *when submitted*.

---

# The `value` Attribute

`value` is what gets submitted for that control:

```html
<input
    type="radio"
    id="uganda"
    name="country"
    value="uganda"
>
<label for="uganda">Uganda</label>
```

If this is selected, the submitted value is `uganda`.

---

# Required Fields

Add `required` when a field must be filled before submission:

```html
<label for="email">Email:</label>

<input
    type="email"
    id="email"
    name="email"
    required
>
```

The browser will block submission until it's done.

---

# Placeholder Text

`placeholder` shows a temporary hint inside the input:

```html
<input
    type="text"
    id="username"
    name="username"
    placeholder="Enter your username"
>
```

It fades when you start typing. It should **not** replace a proper `<label>` — labels are always needed.

---

# The Submit Button

You need a way to send the form:

```html
<button type="submit">Submit</button>
```

That `type="submit"` is the signal to the browser: "submit this form."

---

# The `<button>` Element

```html
<button>Click Me</button>
```

Inside forms, be explicit:

```html
<button type="submit">Submit</button>
```

For a button that *doesn't* submit (e.g. JS actions):

```html
<button type="button">Click Me</button>
```

---

# Form Submission — `action` and `method`

`action` says **where** the data goes:

```html
<form action="/register">
    ...
</form>
```

`method` says **how**:

```html
<form action="/register" method="post">
    ...
</form>
```

```html
<form action="/search" method="get">
    ...
</form>
```

* `GET` — requesting/searching; values may appear in the URL. Good for searches.
* `POST` — creating/changing data; values go in the request body. Good for registrations, logins.

---

# Complete Example

```html
<form action="/register" method="post">

    <h2>Create an Account</h2>

    <label for="name">Name:</label>
    <input
        type="text"
        id="name"
        name="name"
        required
    >

    <br>

    <label for="email">Email:</label>
    <input
        type="email"
        id="email"
        name="email"
        required
    >

    <br>

    <label for="password">Password:</label>
    <input
        type="password"
        id="password"
        name="password"
        required
    >

    <br>

    <label for="country">Country:</label>

    <select id="country" name="country">
        <option value="uganda">Uganda</option>
        <option value="kenya">Kenya</option>
        <option value="tanzania">Tanzania</option>
    </select>

    <br>

    <label for="message">About You:</label>

    <textarea
        id="message"
        name="message"
        rows="5"
        cols="40"
    ></textarea>

    <br>

    <button type="submit">Register</button>

</form>
```

---

# Grouping Controls — `<fieldset>` and `<legend>`

For larger forms, group related fields:

```html
<fieldset>

    <legend>Personal Information</legend>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

</fieldset>
```

`<fieldset>` is the group; `<legend>` is its title.

---

# At a glance

| Element / Attribute | What it does |
| ------------------- | ------------ |
| `<form>` | Wraps the form |
| `<label>` | Describes a form control |
| `<input>` | Creates an input |
| `<textarea>` | Multi-line text input |
| `<select>` | Drop-down list |
| `<option>` | An option in the list |
| `<button>` | Clickable button |
| `<fieldset>` | Groups related controls |
| `<legend>` | Title for a fieldset |
| `type` | Kind of input or button |
| `id` | Identity in the page |
| `name` | Name sent on submission |
| `value` | Value submitted |
| `required` | Must be completed |
| `placeholder` | Temporary hint |
| `action` | Where data is sent |
| `method` | How data is sent |

# Recap

Core shape:

```html
<form>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <button type="submit">Submit</button>

</form>
```

Structure within:

```text
<form>
    ├── <label>
    ├── <input>
    ├── <textarea>
    ├── <select>
    │     └── <option>
    └── <button>
</form>
```

Forms give you **the structure for collecting information**. HTML defines the fields and what they mean; the server then receives and does something with that data.
