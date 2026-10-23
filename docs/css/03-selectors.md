# Selectors

A selector tells the browser which elements a rule applies to. Good selectors keep CSS small and predictable.

## Type selectors

A type selector targets an element name:

```css
p {
  color: #333;
}

h2 {
  margin-top: 2rem;
}
```

Use type selectors for base styles that should apply everywhere.

## Class selectors

A class selector targets elements with a matching `class` attribute. The dot is part of the selector:

```html
<p class="lead">Fresh bread is baked every morning.</p>
```

```css
.lead {
  font-size: 1.125rem;
  color: #444;
}
```

Classes can be reused on many elements. They are the main tool for component styles.

## ID selectors

An id selector targets one element:

```html
<header id="site-header">...</header>
```

```css
#site-header {
  background: #111;
  color: #fff;
}
```

An `id` must be unique on the page. Avoid using ids for routine styling because they have high specificity and are hard to override later. Use them for in-page links and JavaScript hooks.

## Grouping selectors

Apply the same declarations to several selectors with a comma:

```css
h1,
h2,
h3 {
  font-weight: 600;
  line-height: 1.2;
}
```

## Descendant and child selectors

```css
/* any <a> inside <nav> */
nav a {
  text-decoration: none;
}

/* only direct <li> children of <ul> */
ul > li {
  margin-bottom: 0.25rem;
}
```

The space is a descendant combinator. The `>` is a child combinator. Use the child combinator when you only want direct children.

## Attribute selectors

```css
/* links that open in a new tab */
a[target="_blank"] {
  text-decoration: underline;
}

/* email inputs */
input[type="email"] {
  border-color: #888;
}
```

Attribute selectors are useful when the attribute itself carries meaning you want to style.

## Choosing a selector

- Use a **class** for a reusable visual style.
- Use a **type selector** for base element styles.
- Use an **id** for a unique anchor or script hook, not for routine styling.
- Keep selectors short. `body main article ul li a` is a sign that the link needs a class.

Pseudo-classes such as `:hover` and pseudo-elements such as `::before` have their own chapters.

## Try it

Add three links to a page: one normal link, one with `class="nav-link"`, and one with `target="_blank"`.

1. Style all links with a type selector.
2. Give `.nav-link` a different colour.
3. Style `a[target="_blank"]` with an underline.
4. Add a rule for `nav a` and check which links it affects.

Use the browser's inspector to see which rule wins.

Next: [Nesting](04-nesting.md)
