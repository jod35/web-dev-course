# Custom Properties

Custom properties, often called CSS variables, let you name a value and reuse it.

## Defining and using

```css
:root {
  --bg: #ffffff;
  --text: #1a1a1a;
  --primary: hsl(220 90% 41%);
  --radius: 0.5rem;
}

body { background: var(--bg); color: var(--text); }
.btn-primary { background: var(--primary); color: #fff; border-radius: var(--radius); }
```

Define on `:root` to make them global.

## Fallbacks

If a variable is missing, `var()` can provide a fallback:

```css
.card { color: var(--text, #222); }
```

## Changing at runtime

Override per component or per state:

```css
.card { --card-bg: #fff; background: var(--card-bg); }
.card.featured { --card-bg: #f0f6ff; }

.btn { background: var(--primary); }
.btn:hover { --primary: hsl(220 90% 36%); }
```

No extra classes needed on the property itself.

## Scoping

A custom property is scoped to its element and inherits to descendants:

```css
.section { --gap: 1rem; }
.section .cards { gap: var(--gap); } /* inherits 1rem */
.section.compact { --gap: 0.5rem; }  /* override for compact sections */
```

## When to use

- Palette, spacing scale, radius, shadows: define once in `:root`.
- Theming: change variables, not every rule.
- Calculations: `calc(var(--gap) * 2)`.

```css
:root {
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-4: 1rem;
}
.stack > * + * { margin-top: var(--space-4); }
```

## Recap

| Need | Write |
|------|-------|
| Define | `--name: value` on `:root` or a selector |
| Use | `var(--name)` or `var(--name, fallback)` |
| Override | Redefine same variable on a narrower selector |
