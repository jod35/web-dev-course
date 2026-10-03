# Selectors

Selectors are how you say “style these elements, not those.” Get them right and your CSS stays small and predictable.

## Type selector

Targets an element name:

```css
p { color: #333; }
h2 { margin-top: 2rem; }
```

## Class selector

Targets a class — the workhorse for most styling. The dot matters:

```html
<p class="lead">Fresh bread daily.</p>
```

```css
.lead {
  font-size: 1.125rem;
  color: #444;
}
```

A class can be reused on many elements. Use it when you want a style you can repeat.

## ID selector

Targets one unique element. Use sparingly, it has very high specificity:

```html
<header id="site-header">...</header>
```

```css
#site-header {
  background: #111;
  color: #fff;
}
```

If you find yourself writing many `#id` selectors, prefer classes.

## Grouping

Same declarations for several selectors:

```css
h1, h2, h3 {
  font-weight: 600;
  line-height: 1.2;
}
```

## Descendant and child

```css
/* any <a> inside <nav> */
nav a { text-decoration: none; }

/* only direct <li> children of <ul> */
ul > li { margin-bottom: 0.25rem; }
```

## Attribute

```css
/* any link that opens in a new tab */
a[target="_blank"] { text-decoration: underline; }

/* email inputs */
input[type="email"] { border-color: #888; }
```

## Pseudo-classes

Style states or positions:

```css
a:hover { color: crimson; }
a:focus-visible { outline: 2px solid #333; }
li:first-child { font-weight: bold; }
input:disabled { opacity: 0.6; }
```

## Pseudo-elements

Style a part of an element:

```css
p::first-line { font-weight: 600; }
blockquote::before { content: "“"; }
```

## Choosing

- Repeatable visual style: use a **class**.
- One-off anchor target: `id` is okay, but do not style by `id` unless you must.
- State or position: **pseudo-class**.
- Keep selectors short. If you write `body main article ul li a`, you probably need a class on the `a` instead.

## Recap

| Selector | Example | When to use |
|----------|---------|-------------|
| Type | `p`, `h1` | Base element defaults |
| Class | `.card`, `.lead` | Most styling |
| ID | `#header` | Unique anchors, not for routine styling |
| Attribute | `[type="email"]` | Style by attribute |
| Pseudo-class | `:hover`, `:focus` | States |
