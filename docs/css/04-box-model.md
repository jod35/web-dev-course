# Box Model

Every element is a rectangular box. That box has four layers from inside out: content, padding, border, margin.

```text
  margin
  ┌─────────────────────┐
  │  border             │
  │  ┌───────────────┐  │
  │  │ padding       │  │
  │  │ ┌───────────┐ │  │
  │  │ │ content   │ │  │
  │  │ └───────────┘ │  │
  │  └───────────────┘  │
  └─────────────────────┘
```

## Seeing it

```html
<div class="card">Hello</div>
```

```css
.card {
  width: 240px;
  padding: 16px;
  border: 2px solid #333;
  margin: 24px;
}
```

`width` sets the content width by default. Padding pushes the border out, margin pushes neighbors away.

## `box-sizing`

The default `content-box` makes `width` ignore padding and border, so the rendered size is `width + padding + border`. That trips people up.

Fix it once at the top of your file:

```css
* { box-sizing: border-box; }

.card {
  width: 240px; /* now includes padding and border */
  padding: 16px;
  border: 2px solid #333;
}
```

Now `240px` is the visible box width. Use this for every project at MHSM.

## Padding vs margin

- **Padding** — space inside the box, between content and border. Background color covers it.
- **Margin** — space outside the box, between this box and the next. Background does not cover it.

```css
.card { padding: 1rem; }   /* breathing room inside */
.stack > * + * { margin-top: 1rem; } /* space between siblings */
```

## Shorthand

```css
/* all four sides */
margin: 1rem;

/* vertical | horizontal */
padding: 0.5rem 1rem;

/* top | horizontal | bottom */
margin: 1rem 0 2rem;

/* top | right | bottom | left */
padding: 1rem 1.5rem 1rem 1.5rem;
```

Same for `border`, plus width/style/color:

```css
.card { border: 1px solid #ddd; }
```

## Margin collapse — the surprise

Vertical margins between block elements collapse. Only the larger one wins:

```css
h2 { margin-bottom: 1rem; }
p  { margin-top: 1rem; }
```

Gap between them is `1rem`, not `2rem`. This is normal. If you need exact control, use padding or a flex/grid gap instead.

## Recap

| Layer | What it does | Background? |
|-------|--------------|-------------|
| Content | Text/image size | Yes |
| Padding | Inner space | Yes |
| Border | Edge line | Yes (border itself) |
| Margin | Outer space | No |

Remember: `* { box-sizing: border-box; }` and think padding for inner space, margin for outer space.
