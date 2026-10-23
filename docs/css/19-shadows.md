# Shadows

Shadows suggest depth. CSS has `box-shadow` for boxes and `text-shadow` for text. Use them sparingly; a page with a shadow on everything becomes harder to read.

## Box shadow

```css
.card {
  box-shadow: 0 1px 3px rgb(0 0 0 / 0.12);
}
```

The syntax is:

```text
offset-x offset-y blur spread color
```

You rarely need spread. A small vertical offset and a soft blur usually look more natural than a large, dark shadow.

```css
.card-elevated {
  box-shadow: 0 4px 12px rgb(0 0 0 / 0.12);
}
```

You can layer two shadows for a more natural result:

```css
.card-layered {
  box-shadow:
    0 1px 2px rgb(0 0 0 / 0.08),
    0 4px 12px rgb(0 0 0 / 0.10);
}
```

## Inset shadows

```css
.pressed {
  box-shadow: inset 0 2px 4px rgb(0 0 0 / 0.12);
}
```

`inset` draws the shadow inside the box.

## Text shadow

```css
.banner-title {
  text-shadow: 0 1px 2px rgb(0 0 0 / 0.25);
}
```

Use text shadow mainly to lift text off a busy image. It is not a substitute for good contrast.

## Keep shadows consistent

```css
:root {
  --shadow-sm: 0 1px 2px rgb(0 0 0 / 0.08);
  --shadow-md: 0 4px 12px rgb(0 0 0 / 0.12);
}

.card {
  box-shadow: var(--shadow-sm);
}
```

A small set of shadow values keeps the interface consistent.

## Try it

1. Add a small shadow to a card.
2. Increase the blur and offset, then reduce them again. Which version is easier to read?
3. Layer two shadows and compare them with a single shadow.
4. Add a text shadow to a title on a dark background.
5. Remove the shadow from body text. Text shadows usually make long text harder to read.

If the shadow looks like a dark border, reduce the opacity and increase the blur.

Next: [Typography](20-typography.md)
