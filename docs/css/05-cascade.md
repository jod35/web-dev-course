# The Cascade

When several rules target the same element, the browser has to choose which declaration wins. That process is the cascade.

For everyday CSS, three things decide the result:

1. Importance
2. Specificity
3. Source order

## Source order

If two rules have the same importance and specificity, the one that appears later wins:

```css
p {
  color: #333;
}

p {
  color: crimson;
}
```

Every paragraph is crimson because the second rule comes later.

The same applies across stylesheets. A stylesheet linked later in `<head>` comes after one linked earlier. A `<style>` block comes after a linked stylesheet if it appears after the `<link>` element.

Put general rules first and overrides later:

```css
/* base */
p {
  color: #333;
  line-height: 1.6;
}

/* later, same specificity, so this wins */
.lead {
  color: #111;
  font-size: 1.125rem;
}
```

Here `.lead` also has higher specificity than `p`, so it wins for elements with that class.

## Importance

`!important` makes a declaration beat normal declarations:

```css
p {
  color: crimson !important;
}
```

Use it rarely. It is useful when you must override CSS you cannot edit, such as a third-party widget. If you need `!important` to beat your own stylesheet, your selectors are probably too specific or your source order is unclear.

## Inline styles

An inline style wins over normal rules in a stylesheet because it applies directly to the element:

```html
<p style="color: crimson;">Hello</p>
```

Avoid inline styles for normal styling. They are difficult to reuse and override.

## Browser defaults

Browsers apply their own default styles before your CSS. That is why headings are bold and lists have bullets without any CSS from you.

Your author styles override browser defaults when they target the same property:

```css
body {
  margin: 0;
  font-family: system-ui, sans-serif;
}
```

Normal user styles and browser accessibility settings also participate in the cascade. For this course, you mainly need importance, specificity, and source order.

## A practical order

Write your CSS from general to specific:

```css
/* 1. base */
body {
  font-family: system-ui, sans-serif;
  color: #222;
}

/* 2. shared components */
.card {
  padding: 1rem;
  border: 1px solid #ddd;
}

/* 3. variants */
.card.featured {
  border-color: #0a58ca;
}
```

## Try it

1. Add two `p` rules with different colours and no extra selectors. Which wins?
2. Change the second selector to `.lead` and add that class to one paragraph. Which paragraphs change?
3. Add an inline style to one paragraph. Which colour wins?
4. Add `!important` to the first rule. What happens now?
5. Remove the inline style and the `!important`, then put the rules back in a sensible order.

Use the browser inspector to see which declarations are crossed out.

Next: [Specificity](06-specificity.md)
