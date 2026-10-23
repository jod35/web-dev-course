# Images

Images can explain something faster than text, but they also need care. An image without useful alt text is invisible to screen reader users, and an image without dimensions can make the page jump while it loads.

The element is `<img>`:

```html
<img src="bread.jpg" alt="A loaf of brown bread on a wooden table">
```

`<img>` is a void element, so it has no closing tag. It has two required attributes in practice: `src` and `alt`.

## `src`: where the image is

`src` is the path to the image file:

```html
<img src="bread.jpg" alt="A loaf of brown bread">
```

If the image is in a folder:

```html
<img src="images/bread.jpg" alt="A loaf of brown bread">
```

You can also use a full URL:

```html
<img src="https://example.com/bread.jpg" alt="A loaf of brown bread">
```

For your own projects, keep images in a folder such as `images/` and use relative paths.

## `alt`: a text description

`alt` describes the image for people who cannot see it. It is used by screen readers, shown when the image fails to load, and read by search engines.

```html
<img src="gorilla.jpg" alt="A mountain gorilla sitting in tall grass">
```

Write what matters about the image in context, not a list of every detail. Ask: if this image were removed, what would the reader miss?

### Images that are only decoration

If an image is purely decorative and the surrounding text already explains everything, use an empty alt:

```html
<img src="divider.png" alt="">
```

Do not write `alt="image"` or `alt="picture of..."`. Those words add no information.

### Images inside links

If an image is the only content of a link, the alt text should describe the destination:

```html
<a href="menu.html">
  <img src="menu-icon.png" alt="See the menu" width="40" height="40">
</a>
```

## Width and height

The `width` and `height` attributes give the browser the image's dimensions:

```html
<img
  src="bread.jpg"
  alt="A loaf of brown bread"
  width="400"
  height="300"
>
```

Providing both helps the browser reserve space before the image loads, which prevents the page from shifting. CSS can change the displayed size later.

## Figures and captions

Use `<figure>` and `<figcaption>` when an image needs a visible caption:

```html
<figure>
  <img
    src="gorilla.jpg"
    alt="A mountain gorilla sitting in tall grass"
    width="500"
    height="350"
  >
  <figcaption>A mountain gorilla in Mgahinga Gorilla National Park.</figcaption>
</figure>
```

- `<figure>` groups the image with its caption.
- `<figcaption>` holds the visible caption.

Alt text and captions do different jobs. Alt text is for people who cannot see the image. The caption is visible to everyone and adds context.

## Check your work

- Does every `<img>` have `src` and `alt`?
- Is the alt text a useful description, not a filename?
- Are purely decorative images marked with `alt=""`?
- Does the image path match the actual file name and folder?
- Do images have `width` and `height` so the page does not jump?
- Does the image still make sense at a narrow window width?

## Try it

Add an image to a page you have already built. Include:

1. a relative path to an image in an `images/` folder,
2. useful alt text,
3. `width` and `height`,
4. a `<figure>` and `<figcaption>` if the image needs a visible caption.

Then temporarily change the file name in `src` and reload. Read the alt text in the broken image. Would someone who cannot see the picture still understand what was there? Fix the path afterwards.

Next: [Lists](14-lists.md)
