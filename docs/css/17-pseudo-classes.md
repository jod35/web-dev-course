# Pseudo-classes

A pseudo-class styles an element in a particular state. Pseudo-classes use a single colon: `:hover`.

## Interaction states

```css
a:hover {
  color: crimson;
}

a:focus-visible {
  outline: 2px solid #333;
  outline-offset: 2px;
}

a:active {
  color: #a00;
}

button:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}
```

Always provide a visible `:focus-visible` style when you change `:hover`. Keyboard users need to see where they are.

Do not remove focus outlines without replacing them. `outline: none` on a link or button makes keyboard navigation much harder.

## Position in a parent

```css
li:first-child {
  font-weight: bold;
}

li:last-child {
  margin-bottom: 0;
}

li:nth-child(2) {
  color: #555;
}

tr:nth-child(even) {
  background: #f9f9f9;
}
```

These selectors count elements among their siblings.

## Form states

```css
input:required {
  border-color: #888;
}

input:valid {
  border-color: #1a7f37;
}

input:invalid {
  border-color: crimson;
}

input:checked + label {
  font-weight: 600;
}
```

Do not rely on colour alone to show validity. Add text or another visible indicator.

## Negation and grouping

```css
/* everything except the first item */
li:not(:first-child) {
  margin-top: 0.5rem;
}

/* any heading inside a card */
.card :is(h2, h3) {
  line-height: 1.2;
}

/* cards that contain an image */
.card:has(img) {
  padding-top: 0;
}
```

`:where()` works like `:is()` but has zero specificity. It is useful when you want a default rule that is easy to override.

## Link order

For older browsers, write link states in this order so later rules do not override earlier ones:

```css
a:link { }
a:visited { }
a:hover { }
a:active { }
```

The order is often remembered as **LoVe HAte**.

## Try it

1. Style a link's normal, hover, focus-visible, and active states.
2. Tab through the page with the keyboard. Can you always see where focus is?
3. Style every second row of a table with `:nth-child(even)`.
4. Add a form input with `required` and style `:valid` and `:invalid`.
5. Add a `.card:has(img)` rule and check which cards it affects.

If a hover style also removes the focus outline, fix `:focus-visible` before continuing.

Next: [Borders](18-borders.md)
