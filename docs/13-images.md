# 13 - Images

## 1. What are Images?

Images are pictures displayed on a webpage. They can make webpages more attractive and help communicate information.

HTML uses the `<img>` element to display images.

```html
<img src="cat.jpg" alt="A cat">
```

---

## 2. The `<img>` Element

The `<img>` element is used to display an image.

```html
<img src="photo.jpg" alt="A beautiful landscape">
```

The `<img>` element does not have a closing tag.

---

## 3. The `src` Attribute

The `src` attribute specifies the **location of the image**.

```html
<img src="cat.jpg" alt="A cat">
```

If the image is inside a folder:

```html
<img src="images/cat.jpg" alt="A cat">
```

The image can also come from a URL:

```html
<img src="https://example.com/cat.jpg" alt="A cat">
```

---

## 4. The `alt` Attribute

The `alt` attribute provides a description of the image.

```html
<img src="dog.jpg" alt="A brown dog">
```

The `alt` text is useful when:

* The image cannot be displayed.
* Someone uses a screen reader.
* The image needs to be described to someone who cannot see it.

---

## 5. Image Width and Height

The `width` attribute controls the width of an image.

```html
<img src="cat.jpg" alt="A cat" width="400">
```

The `height` attribute controls the height.

```html
<img src="cat.jpg" alt="A cat" width="400" height="300">
```

Both attributes can be used together.

---

## 6. Images in Folders

Images are often stored in a separate folder.

```text
website/
├── index.html
└── images/
    ├── cat.jpg
    └── dog.jpg
```

To display `cat.jpg`:

```html
<img src="images/cat.jpg" alt="A cat">
```

---

## 7. Image Captions

A caption is visible text that describes or identifies an image.

HTML provides `<figure>` and `<figcaption>` for images with captions.

```html
<figure>
    <img src="cat.jpg" alt="A sleeping cat">
    <figcaption>A cat sleeping on a chair.</figcaption>
</figure>
```

### `<figure>`

Groups an image and its caption together.

### `<figcaption>`

Contains the visible caption.

---

## 8. `alt` Text vs Caption

`alt` text and captions have different purposes.

```html
<figure>
    <img src="elephant.jpg" alt="An elephant walking through grass">
    <figcaption>An elephant in Queen Elizabeth National Park.</figcaption>
</figure>
```

**`alt`**

Provides a description of the image, mainly for accessibility and when the image cannot be displayed.

**`figcaption`**

Provides a visible caption that appears with the image.

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

### Important attributes and elements

| Element/Attribute | Purpose                              |
| ----------------- | ------------------------------------ |
| `<img>`           | Displays an image                    |
| `src`             | Specifies the image location         |
| `alt`             | Describes the image                  |
| `width`           | Sets the image width                 |
| `height`          | Sets the image height                |
| `<figure>`        | Groups an image with related content |
| `<figcaption>`    | Adds a visible image caption         |
