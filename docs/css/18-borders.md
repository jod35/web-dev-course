# Borders

A border is a line around a box. It has a width, a style, and a colour.

## Shorthand

```css
.card {
  border: 1px solid #ddd;
}
```

This is equivalent to:

```css
.card {
  border-width: 1px;
  border-style: solid;
  border-color: #ddd;
}
```

A border needs a style. `border-width: 1px` without `solid`, `dashed`, or another style will not show a line.

## Individual sides

```css
.card {
  border-top: 2px solid #0a58ca;
}
```

You can use physical sides (`top`, `right`, `bottom`, `left`) or logical sides:

```css
.card {
  border-inline-start: 3px solid #0a58ca;
}
```

The logical version follows the writing direction.

## Rounded corners

```css
.card {
  border-radius: 0.5rem;
}

.avatar {
  border-radius: 50%;
}

.pill {
  border-radius: 999px;
}
```

Individual corners are also available:

```css
.card {
  border-top-left-radius: 0.5rem;
  border-top-right-radius: 0.5rem;
}
```

The logical form is `border-start-start-radius`.

## Border or outline?

- **Border** takes up space and affects layout.
- **Outline** is drawn outside the box, does not affect layout, and is useful for focus states.

```css
:focus-visible {
  outline: 2px solid #333;
  outline-offset: 2px;
}
```

Do not remove an outline unless you replace it with an equally visible focus style.

## Try it

1. Add a border to a card and change its width, style, and colour.
2. Add a thick border on one side only.
3. Try `border-radius` with a small value and with `50%`.
4. Add a focus outline to a button and tab to it with the keyboard.
5. Set `outline-offset` to `0` and then `4px`. Which is easier to see?

If a border does not appear, check whether the style is missing or the colour matches the background.

Next: [Shadows](19-shadows.md)
