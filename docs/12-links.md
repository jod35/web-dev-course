# Links

## 1. What are Links?

Links are how users **jump from one place to another** on the web.

HTML uses the `<a>` element, the **anchor**, for that:

```html
<a href="about.html">About Us</a>
```

The text "About Us" is what the visitor actually clicks.

---

## 2. The `<a>` Element

A hyperlink is just an `<a>` with a destination:

```html
<a href="https://www.google.com">Google</a>
```

Breaking it down:

* `<a>`: the anchor element
* `href`: where it points
* `Google`: the clickable label

---

## 3. The `href` Attribute

`href` says **where the link goes**:

```html
<a href="about.html">About Us</a>
```

That destination could be:

* another page on your site
* a page on a different website
* a spot on the same page
* an email address

---

## 4. Linking to Another Website

Use the full URL:

```html
<a href="https://www.wikipedia.org">Wikipedia</a>
```

```html
<a href="https://www.python.org">Python</a>
```

---

## 5. Linking to Another Page on Your Site

Say your site looks like this:

```text
website/
├── index.html
├── about.html
└── contact.html
```

From `index.html` you can point to the others directly:

```html
<a href="about.html">About Us</a>
```

```html
<a href="contact.html">Contact Us</a>
```

---

## 6. Linking to a Page Inside a Folder

If the target lives in a folder, include that folder in the path:

```text
website/
├── index.html
└── pages/
    ├── about.html
    └── contact.html
```

```html
<a href="pages/about.html">About Us</a>
```

---

## 7. Opening a Link in a New Tab

Want the link to open elsewhere? Add `target`:

```html
<a href="https://www.python.org" target="_blank">
    Python
</a>
```

`target="_blank"` usually opens a new tab, handy for external sites so you don't pull people away from yours.

---

## 8. Linking to an Email Address

Use the `mailto:` scheme:

```html
<a href="mailto:example@email.com">
    Send me an email
</a>
```

Clicking it will try to open the visitor's email app.

---

## 9. Linking to a Specific Spot on a Page

Give an element an `id` first:

```html
<h2 id="contact">Contact Us</h2>
```

Then link to it with a hash:

```html
<a href="#contact">Go to Contact Us</a>
```

That `#` tells the browser "find the element with this id and scroll to it."

---

## 10. Linking an Image

An image can be the clickable thing too:

```html
<a href="about.html">
    <img src="images/logo.png" alt="About Us" width="200">
</a>
```

Click the image → go to `about.html`.

---

## 11. Navigation Links

Put those `<a>`s together and you've got site navigation:

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="services.html">Services</a>
    <a href="contact.html">Contact</a>
</nav>
```

That's how users move between pages, simple, but essential.

---

## 12. Putting It Together

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>

<body>

    <h1>My Website</h1>

    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
        <a href="contact.html">Contact</a>
    </nav>

    <h2>Welcome</h2>

    <p>
        Visit the
        <a href="https://www.python.org">Python website</a>
        to learn more about Python.
    </p>

</body>
</html>
```

### At a glance

| Element / Attribute | What it's for |
| ------------------- | ------------- |
| `<a>` | Creates a link |
| `href` | Where the link points |
| `target` | Where to open it |
| `target="_blank"` | Open in a new tab/window |
| `mailto:` | Make it an email link |
| `#id` | Jump to an element on the page |
