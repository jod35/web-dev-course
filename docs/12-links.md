# Links

Links let readers move between pages, jump to a section, or send an email. HTML uses the anchor element, `<a>`, for all of these.

```html
<a href="menu.html">See the menu</a>
```

- `<a>` creates the link.
- `href` says where the link goes.
- The text between the tags is what readers click.

## Linking to another website

Use the full URL, including `https://`:

```html
<p>Visit the <a href="https://www.python.org">Python website</a>.</p>
```

This is an absolute URL because it contains the full address.

## Linking to your own pages

Use a relative path when the target is part of your site:

```text
website/
├── index.html
├── menu.html
└── contact.html
```

```html
<a href="menu.html">Menu</a>
<a href="contact.html">Contact</a>
```

If the file is inside a folder, include the folder name:

```text
website/
├── index.html
└── pages/
    ├── menu.html
    └── contact.html
```

```html
<a href="pages/menu.html">Menu</a>
```

The path is relative to the page containing the link. A broken link is usually a filename or folder mistake.

## Opening a link in a new tab

Add `target="_blank"` to open the link in a new tab:

```html
<a href="https://www.python.org" target="_blank" rel="noopener">Python</a>
```

Only do this for links where leaving the page would interrupt the reader. Avoid opening every link in a new tab. When you use `target="_blank"`, add `rel="noopener"` so the new page cannot control the original tab through `window.opener`.

## Linking to an email address

Use `mailto:`:

```html
<a href="mailto:webclub@example.com">Email the web club</a>
```

The browser will try to open the reader's email application.

## Linking to a section on the same page

Give the target element an `id`, then link to it with `#`:

```html
<h2 id="contact">Contact</h2>

<p><a href="#contact">Go to contact details</a></p>
```

The `id` must be unique on the page. The link scrolls to the element with that id.

## Linking an image

An image can be the clickable content:

```html
<a href="menu.html">
  <img src="images/bread.jpg" alt="See the bread menu" width="300">
</a>
```

If the image is the only content of the link, its alt text should describe the link destination.

## Navigation

A group of links can become site navigation:

```html
<nav>
  <a href="index.html">Home</a>
  <a href="menu.html">Menu</a>
  <a href="contact.html">Contact</a>
</nav>
```

`<nav>` is covered in the page landmarks chapter. For now, remember that navigation is still a group of links.

## Complete example

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>MHSM Bakery</title>
</head>
<body>
  <h1>MHSM Bakery</h1>

  <nav>
    <a href="index.html">Home</a>
    <a href="menu.html">Menu</a>
    <a href="contact.html">Contact</a>
  </nav>

  <p>
    Read about our bread on the <a href="menu.html">menu page</a>.
  </p>

  <p>
    You can also visit the
    <a href="https://www.python.org" target="_blank" rel="noopener">Python website</a>.
  </p>
</body>
</html>
```

## Check your work

- Click every link. It should go to the page or section you expected.
- Check the spelling and capitalisation of file names. `Menu.html` and `menu.html` are different on many servers.
- Do not use "click here" as link text. Describe the destination instead.
- Add `rel="noopener"` when you use `target="_blank"`.

## Try it

Create two pages, `index.html` and `contact.html`, in the same folder. On `index.html`:

1. Add a `<nav>` with a link to `contact.html`.
2. Add a link to an external website.
3. Add a section with `id="hours"` and a link that jumps to it.
4. Add a `mailto:` link.

Open the page and test each link. Then rename `contact.html` to `contact-us.html` without updating the link and see what the browser reports. Fix the link afterwards.

Next: [Images](13-images.md)
