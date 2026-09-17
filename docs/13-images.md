# 13,Images

**Goal:** embed images accessibly with `img`,and caption them with `figure`.

## The tag

`src` is the file, `alt` is the **text replacement**. `alt` is effectively required,screen readers read it, search engines index it, and it shows when the image fails:

```html
<img src="bread.jpg" alt="Fresh loaves on a wooden shelf">
```

## Writing good `alt`

| Image | `alt` |
|-------|-------|
| Informative photo | Describe the content: `"Fresh loaves on a wooden shelf"` |
| Decorative border | Empty: `alt=""` so readers skip it |
| Image link | Describe the destination: `alt="Our menu (PDF)"`, not "image" |

## Size and paths

```html
<img src="images/bread.jpg" alt="Fresh loaves" width="600">
```

- `src` paths follow the same relative/absolute rules as links (Chapter 12).
- `width` (and `height`) reserve layout space so the page doesn't jump while loading. Fine-tune display size with CSS later.

## Captions with `figure`

To attach a visible caption, wrap in `<figure>` with `<figcaption>`:

```html
<figure>
  <img src="oven.jpg" alt="Baker sliding loaves into a stone oven">
  <figcaption>Morning bake, 5am.</figcaption>
</figure>
```

`<figcaption>` must be the first or last child of `<figure>`.

## Clickable images

```html
<a href="menu.html"><img src="menu-thumb.jpg" alt="Our menu"></a>
```

The `alt` describes **where the link goes**, not the pixels.

## Gotchas

- Never omit `alt`,validators flag it and readers suffer.
- Huge photo files slow the page; resize before publishing (CSS can't shrink bytes).
- `title` on images is not a substitute for `alt`.

## Recap

| Attribute/Tag | Job |
|---------------|-----|
| `src` | Image file path |
| `alt` | Text replacement,always present |
| `figure`/`figcaption` | Image + visible caption |
| Linked `<img>` | `alt` = link destination |

**Next:** [14,Lists](14-lists.md) · **Prev:** [12,Links](12-links.md)
