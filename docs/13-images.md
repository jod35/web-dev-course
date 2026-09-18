# 13 - Images

**Goal:** In this chapter you will learn how to embed images accessibly with `img`, and how to caption them with `figure`.

## The tag

The `src` attribute provides the image file, while the `alt` attribute provides the **text replacement**. The `alt` attribute is effectively required, because screen readers read it, search engines index it, and browsers show it when the image fails to load:

```html
<img src="bread.jpg" alt="Fresh loaves on a wooden shelf">
```

## Writing good `alt`

| Image | `alt` |
|-------|-------|
| Informative photo | Describe the content: `"Fresh loaves on a wooden shelf"` |
| Decorative border | Leave it empty with `alt=""` so that readers skip it |
| Image link | Describe the destination, for example `alt="Our menu (PDF)"` instead of "image" |

## Size and paths

```html
<img src="images/bread.jpg" alt="Fresh loaves" width="600">
```

- The `src` paths follow the same relative and absolute rules as links, as explained in Chapter 12.
- The `width` attribute, together with `height`, reserves layout space so that the page does not jump while it loads. Fine-tune the display size later with CSS.

## Captions with `figure`

To attach a visible caption to an image, wrap the image in a `<figure>` element with a `<figcaption>` element:

```html
<figure>
  <img src="oven.jpg" alt="Baker sliding loaves into a stone oven">
  <figcaption>Morning bake, 5am.</figcaption>
</figure>
```

The `<figcaption>` element must be the first or the last child of the `<figure>` element.

## Clickable images

```html
<a href="menu.html"><img src="menu-thumb.jpg" alt="Our menu"></a>
```

In this case the `alt` text describes **where the link goes**, not the appearance of the pixels.

## Rules

- Never omit the `alt` attribute, because validators flag the omission and readers suffer the loss.
- Large photo files slow down the page, so resize images before you publish them, since CSS cannot shrink the number of bytes.
- The `title` attribute on images is not a substitute for `alt`.

## Recap

| Attribute/Tag | Job |
|---------------|-----|
| `src` | Image file path |
| `alt` | Text replacement, which is always present |
| `figure`/`figcaption` | Image with a visible caption |
| Linked `<img>` | `alt` text states the link destination |

**Next:** [14 - Lists](14-lists.md) · **Prev:** [12 - Links](12-links.md)
