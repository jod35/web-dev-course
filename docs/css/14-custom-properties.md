# Custom Properties

Custom properties, often called CSS variables, let you name a value and reuse it.

## Defining and using a custom property

```css
:root {
  --bg: #ffffff;
  --text: #1a1a1a;
  --primary: hsl(220 90% 41%);
  --radius: 0.5rem;
}

body {
  background: var(--bg);
  color: var(--text);
}

.btn-primary {
  background: var(--primary);
  color: #fff;
  border-radius: var(--radius);
}
```

Define global values on `:root`. Use `var(--name)` to read them.

## Fallbacks

If a custom property is missing, `var()` can provide a fallback:

```css
.card {
  color: var(--text, #222);
}
```

The fallback is used only when the property is not defined.

## Overriding values

A custom property can be redefined on a smaller part of the page:

```css
.card {
  --card-bg: #fff;
  background: var(--card-bg);
}

.card.featured {
  --card-bg: #f0f6ff;
}
```

The `background` declaration stays the same. Only the value of `--card-bg` changes.

You can also change a variable in a state:

```css
.btn {
  background: var(--primary);
}

.btn:hover {
  --primary: hsl(220 90% 36%);
}
```

## Scoping

Custom properties are scoped to the element where they are defined and inherit to descendants:

```css
.section {
  --gap: 1rem;
}

.section .cards {
  gap: var(--gap);
}

.section.compact {
  --gap: 0.5rem;
}
```

The compact section changes the gap without writing a new rule for `.cards`.

## When to use them

- Palette, spacing scale, radius, and shadows: define once on `:root`.
- Theming: change a few variables instead of every rule.
- Calculations: `calc(var(--gap) * 2)`.

```css
:root {
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-4: 1rem;
}

.stack > * + * {
  margin-top: var(--space-4);
}
```

## Try it

1. Define a colour palette and a spacing scale on `:root`.
2. Use the variables for a button, a card, and a stack of paragraphs.
3. Add a `.compact` class that overrides the spacing variable.
4. Change the primary colour in one place and check that every component updates.
5. Add a fallback to one `var()` and remove the variable temporarily to see it work.

If a variable does not work, check for a missing `--`, a typo in the name, or a definition that is outside the element's scope.

Next: [Spacing](15-spacing.md)
