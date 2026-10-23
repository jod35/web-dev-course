# Color

CSS has several ways to write a colour. Pick a small palette and use it consistently.

## Hex

Hex values are compact and common for fixed colours:

```css
.card {
  background: #0a58ca;
  color: #ffffff;
}
```

When each pair of digits repeats, you can shorten the value: `#fff` is the same as `#ffffff`.

## RGB

RGB lets you set the red, green, and blue channels directly:

```css
.card {
  background: rgb(10 88 202);
}

.card {
  background: rgb(10 88 202 / 0.8);
}
```

The second value has 80% opacity.

## HSL

HSL uses hue, saturation, and lightness:

```css
.btn {
  background: hsl(220 90% 41%);
}

.btn:hover {
  background: hsl(220 90% 48%);
}
```

Hue is the colour family, saturation is how strong it is, and lightness controls how light or dark it is. HSL is convenient when you want to make a colour lighter or darker.

## `currentColor` and transparency

```css
.card {
  border: 1px solid currentColor;
}

.ghost {
  background: transparent;
}
```

`currentColor` uses the element's text colour. It keeps a border or icon in sync with the text.

## A palette with custom properties

Define colours once and reuse them:

```css
:root {
  --bg: #ffffff;
  --text: #1a1a1a;
  --muted: #6b7280;
  --primary: hsl(220 90% 41%);
}

body {
  color: var(--text);
  background: var(--bg);
}

.btn-primary {
  background: var(--primary);
  color: #fff;
}
```

Custom properties are covered in detail later.

## Contrast matters

Text must be readable against its background. Light grey text on white is a common problem:

```css
/* avoid for body text */
.muted {
  color: #ccc;
}
```

Check contrast with a tool or the browser's accessibility panel. Aim for at least 4.5:1 for normal text. Large text can use a lower ratio, but it should still be comfortable to read.

Do not use colour alone to communicate meaning. Add text, an icon, or another visible difference.

## Try it

1. Create a page with a heading, a paragraph, and a button.
2. Define a four-colour palette with custom properties.
3. Use hex for the background, `hsl()` for the button, and `currentColor` for a border.
4. Hover the button and change its lightness slightly.
5. Check the text contrast in the browser's accessibility tools. If the text is hard to read, adjust the palette.

If a colour is hard to reuse, move it into a custom property.

Next: [Sizing](09-sizing.md)
