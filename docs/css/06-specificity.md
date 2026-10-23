# Specificity

Specificity decides which selector wins when two rules have the same importance. It is often written as a three-part score:

```text
[id, class, type]
```

## Reading the score

```text
p              [0,0,1]
.lead          [0,1,0]
p.lead         [0,1,1]
#intro         [1,0,0]
nav a:hover    [0,1,2]
```

- The id column beats everything to its right.
- The class column beats the type column.
- A later rule only wins when both rules have the same score.

One id beats any number of classes:

```css
#intro {
  color: crimson;
}

.lead {
  color: blue;
}
```

The `#intro` rule wins even if `.lead` comes later.

## Keep specificity low

- Prefer classes.
- Avoid id selectors for styling.
- Do not nest selectors deeply.
- To override a rule, add another class rather than `!important`.

```css
/* base */
.btn {
  padding: 0.5rem 1rem;
  border: none;
}

/* variant, same specificity, later wins */
.btn-primary {
  background: #0a58ca;
  color: #fff;
}
```

```html
<button class="btn btn-primary">Save</button>
```

## A common mistake

```css
/* too specific from the start */
#header nav ul li a {
  color: crimson;
}
```

If you later need a different colour for one link, you have to write an even more specific selector. Prefer:

```css
.nav-link {
  color: crimson;
}

.nav-link:hover {
  color: #a00;
}
```

Short selectors are easier to read and easier to override.

## Try it

1. Create a paragraph with `id="intro"` and `class="lead"`.
2. Write a `p` rule, a `.lead` rule, and an `#intro` rule, each with a different colour.
3. Predict which colour wins. Check in the browser.
4. Remove the id rule and predict again.
5. Rewrite the styles so the paragraph uses only a class and the result is still clear.

If you need a chain of ids and `!important` to change one element, simplify the selectors instead.

Next: [Inheritance](07-inheritance.md)
