# 16 - Forms Basics

**Goal:** In this chapter, you will learn how to create forms that allow users to **enter and submit information**. You will learn how forms work, how to create different types of inputs, how to label fields, and how to group related form controls.

## What is an HTML Form?

An HTML form is a section of a webpage where users can **enter or select information**.

Forms are commonly used for:

* Login pages
* Registration
* Contact forms
* Search boxes
* Surveys
* Feedback
* Ordering products
* Booking services

A simple form might look like this:

```html
<form>
    <label for="name">Name:</label>
    <input type="text" id="name">

    <button type="submit">Submit</button>
</form>
```

---

# `<form>` - Form Container

The `<form>` element defines a form.

```html
<form>

    <!-- Form controls go here -->

</form>
```

The elements used to collect information are placed inside the `<form>`.

A form can contain:

* `<input>`
* `<label>`
* `<textarea>`
* `<select>`
* `<option>`
* `<button>`
* `<fieldset>`
* `<legend>`

---

# `<label>` - Describing a Form Control

The `<label>` element provides a description for a form control.

```html
<label for="name">Name:</label>
<input type="text" id="name">
```

The `for` attribute of the label should match the `id` of the input.

```text
for="name"
     ↓
id="name"
```

This connects the label to the input.

Clicking the label can also focus the associated input.

---

# `<input>` - User Input

The `<input>` element is used to collect many different types of information.

```html
<input type="text">
```

The `type` attribute determines what kind of input the browser should provide.

Some common types are:

| Type       | Purpose                 |
| ---------- | ----------------------- |
| `text`     | General text            |
| `email`    | Email address           |
| `password` | Password                |
| `number`   | Number                  |
| `date`     | Date                    |
| `time`     | Time                    |
| `checkbox` | Multiple choices        |
| `radio`    | One choice from a group |
| `file`     | File upload             |
| `search`   | Search input            |
| `submit`   | Form submission         |

---

# Text Input

The `text` type is used for general text.

```html
<label for="name">Name:</label>
<input type="text" id="name">
```

For example, a user could enter:

```text
Jonathan
```

---

# Email Input

The `email` type is intended for email addresses.

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

Browsers can provide appropriate validation and input behavior for email addresses.

---

# Password Input

The `password` type is used for passwords.

```html
<label for="password">Password:</label>
<input type="password" id="password">
```

The characters entered are normally hidden from view.

---

# Number Input

The `number` type is used for numerical values.

```html
<label for="age">Age:</label>
<input type="number" id="age">
```

You can also specify a minimum and maximum value:

```html
<input type="number" id="age" min="10" max="100">
```

---

# Date Input

The `date` type allows the user to select a date.

```html
<label for="birthday">Date of Birth:</label>
<input type="date" id="birthday">
```

The browser may provide a date picker.

---

# Time Input

The `time` type allows the user to select a time.

```html
<label for="appointment">Appointment Time:</label>
<input type="time" id="appointment">
```

---

# Textarea

The `<textarea>` element is used when the user needs to enter **multiple lines of text**.

```html
<label for="message">Message:</label>

<textarea id="message"></textarea>
```

Unlike `<input>`, `<textarea>` has an opening and closing tag.

You can specify its initial size using `rows` and `cols`:

```html
<textarea id="message" rows="5" cols="40"></textarea>
```

---

# Select and Option

The `<select>` element creates a **drop-down list**.

The `<option>` element defines the choices.

```html
<label for="country">Country:</label>

<select id="country">
    <option>Uganda</option>
    <option>Kenya</option>
    <option>Tanzania</option>
    <option>Rwanda</option>
</select>
```

The user can select one of the available options.

---

# Radio Buttons

Radio buttons allow the user to select **one option from a group**.

```html
<p>Gender:</p>

<input type="radio" id="male" name="gender" value="male">
<label for="male">Male</label>

<input type="radio" id="female" name="gender" value="female">
<label for="female">Female</label>
```

The important part is that the radio buttons have the same `name`:

```html
name="gender"
```

This tells the browser that they belong to the same group.

---

# Checkboxes

Checkboxes allow users to select **multiple options**.

```html
<p>Languages you know:</p>

<input type="checkbox" id="python" name="language" value="python">
<label for="python">Python</label>

<input type="checkbox" id="javascript" name="language" value="javascript">
<label for="javascript">JavaScript</label>

<input type="checkbox" id="java" name="language" value="java">
<label for="java">Java</label>
```

Unlike radio buttons, multiple checkboxes can be selected.

---

# The `name` Attribute

The `name` attribute gives a form control a name that can be used when the form data is submitted.

```html
<input type="text" name="username">
```

For example:

```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

Here:

* `id` identifies the element within the HTML document.
* `name` identifies the field when form data is submitted.

---

# The `value` Attribute

The `value` attribute specifies the value associated with a form control.

```html
<input
    type="radio"
    id="uganda"
    name="country"
    value="uganda"
>
<label for="uganda">Uganda</label>
```

If the user selects this option, its value is:

```text
uganda
```

---

# Required Fields

The `required` attribute tells the browser that a field must be completed before the form can be submitted.

```html
<label for="email">Email:</label>

<input
    type="email"
    id="email"
    name="email"
    required
>
```

The browser will prevent submission if the required field has not been completed.

---

# Placeholder Text

The `placeholder` attribute provides a temporary hint inside an input.

```html
<input
    type="text"
    id="username"
    name="username"
    placeholder="Enter your username"
>
```

The placeholder disappears when the user starts entering information.

A placeholder should not replace a proper `<label>`.

---

# The Submit Button

A form usually needs a button that allows the user to submit the information.

```html
<button type="submit">Submit</button>
```

The `type="submit"` tells the browser that the button submits the form.

---

# The `<button>` Element

The `<button>` element creates a clickable button.

```html
<button>Click Me</button>
```

For forms, it is good practice to explicitly specify the button type:

```html
<button type="submit">Submit</button>
```

A button can also be used for other actions, such as:

```html
<button type="button">Click Me</button>
```

---

# Form Submission

The `<form>` element can use `action` to specify **where the form data should be sent**.

```html
<form action="/register">
    ...
</form>
```

The `method` attribute specifies how the browser should submit the data.

Two commonly used methods are:

```html
<form action="/register" method="post">
    ...
</form>
```

and:

```html
<form action="/search" method="get">
    ...
</form>
```

### `GET`

`GET` is commonly used when requesting or searching for information.

The submitted values can appear in the URL.

### `POST`

`POST` is commonly used when submitting information that changes or creates data.

The submitted values are sent in the request body.

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

# Grouping Form Controls

The `<fieldset>` element groups related form controls together.

The `<legend>` element provides a title for the group.

```html
<fieldset>

    <legend>Personal Information</legend>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

</fieldset>
```

This is particularly useful for larger forms.

---

# Important Elements and Attributes

| Element/Attribute | Purpose                                     |
| ----------------- | ------------------------------------------- |
| `<form>`          | Defines a form                              |
| `<label>`         | Describes a form control                    |
| `<input>`         | Creates an input control                    |
| `<textarea>`      | Creates a multi-line text input             |
| `<select>`        | Creates a drop-down list                    |
| `<option>`        | Creates an option in a select list          |
| `<button>`        | Creates a button                            |
| `<fieldset>`      | Groups related form controls                |
| `<legend>`        | Describes a fieldset                        |
| `type`            | Specifies the type of input or button       |
| `id`              | Identifies an element                       |
| `name`            | Names a form field for submission           |
| `value`           | Specifies the value submitted for a control |
| `required`        | Makes a field required                      |
| `placeholder`     | Provides a temporary input hint             |
| `action`          | Specifies where form data is submitted      |
| `method`          | Specifies how form data is submitted        |

# Recap

The basic structure of a form is:

```html
<form>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <button type="submit">Submit</button>

</form>
```

The most important relationship to remember is:

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

A form provides the **structure for collecting information**. HTML defines the fields and their meaning, while a server-side application can receive and process the submitted data.

**Next:** [17 - Grouping: div, section, span](17-div-section.md) · **Prev:** [15 - Tables](15-tables.md)
