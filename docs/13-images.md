# Images

## 1. What are Images?

Pictures on a page make it more inviting and can explain things words alone can't. HTML uses a single element for that:

```html
<img src="cat.jpg" alt="A cat">
```

---

## 2. The `<img>` Element

```html
<img src="photo.jpg" alt="A beautiful landscape">
```

Notice there's no closing tag — `<img>` is a void element. It sits there and displays the image.

---

## 3. The `src` Attribute

`src` tells the browser **where to find the image**:

```html
<img src="cat.jpg" alt="A cat">
```

In a folder?

```html
<img src="images/cat.jpg" alt="A cat">
```

Or out on the web:

```html
<img src="https://example.com/cat.jpg" alt="A cat">
```

---

## 4. The `alt` Attribute

`alt` is the text description for the image:

```html
<img src="dog.jpg" alt="A brown dog">
```

You'll need it when:

* the image fails to load,
* someone is using a screen reader,
* you need a text fallback for any other reason.

Think of it as "what would I say if I had to describe this image over the phone?"

---

## 5. Image Width and Height

`width` sets the display width:

```html
<img src="cat.jpg" alt="A cat" width="400">
```

`height` does the same vertically:

```html
<img src="cat.jpg" alt="A cat" width="400" height="300">
```

You can use one or both — browsers will scale accordingly.

---

## 6. Images in Folders

Most sites keep images tidily in a folder:

```text
website/
├── index.html
└── images/
    ├── cat.jpg
    └── dog.jpg
```

Referencing `cat.jpg` from `index.html`:

```html
<img src="images/cat.jpg" alt="A cat">
```

---

## 7. Image Captions

A caption is the visible text you see under a picture. HTML pairs `<figure>` and `<figcaption>` for that:

```html
<figure>
    <img src="cat.jpg" alt="A sleeping cat">
    <figcaption>A cat sleeping on a chair.</figcaption>
</figure>
```

* `<figure>` groups the image and its caption.
* `<figcaption>` holds the caption text itself.

---

## 8. `alt` Text vs Caption — Not the Same Job

```html
<figure>
    <img src="elephant.jpg" alt="An elephant walking through grass">
    <figcaption>An elephant in Queen Elizabeth National Park.</figcaption>
</figure>
```

* **`alt`** — functional description, for accessibility and when the image can't be shown.
* **`figcaption`** — visible caption the reader sees alongside the image.

You'll often need both.

---

## 9. Complete Example

```html
<figure>
    <img
        src="images/mountain.jpg"
        alt="A mountain surrounded by trees"
        width="500"
    >

    <figcaption>
        A mountain surrounded by trees.
    </figcaption>
</figure>
```

### At a glance

| Element / Attribute | Role |
| ------------------- | ---- |
| `<img>` | Displays an image |
| `src` | Where the image lives |
| `alt` | Text description |
| `width` | Display width |
| `height` | Display height |
| `<figure>` | Groups image with its caption |
| `<figcaption>` | The visible caption |
