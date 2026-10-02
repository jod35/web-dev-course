# 12 - Links

## 1. What are Links?

Links allow users to **move from one webpage or location to another**.

HTML uses the `<a>` element, also called the **anchor element**, to create links.

```html
<a href="about.html">About Us</a>
```

The text **About Us** is what the user clicks.

---

## 2. The `<a>` Element

The `<a>` element creates a hyperlink.

```html
<a href="https://www.google.com">Google</a>
```

The link has:

* `<a>`: the anchor element
* `href`: specifies where the link goes
* `Google`: the clickable text

---

## 3. The `href` Attribute

The `href` attribute specifies the **destination of the link**.

```html
<a href="about.html">About Us</a>
```

The destination can be:

* Another webpage
* Another page in the same website
* A different website
* A specific location on the same page
* An email address

---

## 4. Linking to Another Website

You can create a link to an external website using its URL.

```html
<a href="https://www.wikipedia.org">Wikipedia</a>
```

Another example:

```html
<a href="https://www.python.org">Python</a>
```

---

## 5. Linking to Another Page

You can link to another HTML page in your website.

Suppose you have:

```text
website/
├── index.html
├── about.html
└── contact.html
```

From `index.html`, you can link to `about.html`:

```html
<a href="about.html">About Us</a>
```

And to `contact.html`:

```html
<a href="contact.html">Contact Us</a>
```

---

## 6. Linking to a Page in a Folder

If the page is inside a folder, include the folder in the path.

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

The `target` attribute can specify where the linked page should open.

```html
<a href="https://www.python.org" target="_blank">
    Python
</a>
```

`target="_blank"` tells the browser to open the link in a new browsing context, commonly a new tab.

---

## 8. Linking to an Email Address

The `mailto:` scheme can be used to create an email link.

```html
<a href="mailto:example@email.com">
    Send me an email
</a>
```

Clicking the link can open the user's email application.

---

## 9. Linking to a Specific Location on a Page

You can link to a particular section of the same page using an `id`.

First, give an element an `id`:

```html
<h2 id="contact">Contact Us</h2>
```

Then create a link to it:

```html
<a href="#contact">Go to Contact Us</a>
```

The `#` tells the browser to look for an element with that `id`.

---

## 10. Linking an Image

An image can also be used as a link.

```html
<a href="about.html">
    <img src="images/logo.png" alt="About Us" width="200">
</a>
```

When the user clicks the image, they are taken to `about.html`.

---

## 11. Navigation Links

Links are commonly used to create website navigation.

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="services.html">Services</a>
    <a href="contact.html">Contact</a>
</nav>
```

Navigation links help users move between the different pages of a website.

---

## 12. Complete Example

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

### Important Elements and Attributes

| Element/Attribute | Purpose                                  |
| ----------------- | ---------------------------------------- |
| `<a>`             | Creates a link                           |
| `href`            | Specifies the link destination           |
| `target`          | Specifies where the link should open     |
| `target="_blank"` | Opens the link in a new browsing context |
| `mailto:`         | Creates an email link                    |
| `#id`             | Links to a specific location on a page   |
