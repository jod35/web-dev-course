# Inheritance

Some properties flow from parent to child automatically, others do not.

## Which inherits?

Inherits: `color`, `font-family`, `font-size`, `line-height`, `text-align`.

Does not inherit: `margin`, `padding`, `border`, `background`, `width`, `display`.

You do not need to memorize the full list, just the idea.

```css
body {
  color: #222;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
}
```

A `p` inside `body` will be `#222` and `system-ui` without you writing it again. A `div` will not get `body`’s margin or padding.

## Controlling it

- `inherit` — take parent’s value:

```css
a { color: inherit; } /* link takes surrounding text color */
```

- `initial` — go back to browser default.
- `unset` — inherit if naturally inherited, otherwise initial.

```css
.card { color: #333; }
.card a { color: inherit; } /* same as card, not default blue */
```

## Why it matters

Set text styles high up, box styles low:

```css
body { color: #222; font-family: system-ui, sans-serif; }
.card { padding: 1rem; border: 1px solid #ddd; background: #fff; }
```

Text inherits, boxes do not, so you avoid repeating font declarations on every element.

## Recap

| Behavior | Examples |
|----------|----------|
| Inherits | `color`, `font`, `line-height` |
| Does not inherit | `margin`, `padding`, `border`, `background` |
| Use `inherit` | When you want child to match parent explicitly |
