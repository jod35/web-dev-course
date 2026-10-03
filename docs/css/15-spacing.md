# Spacing

Spacing is how you add breathing room. Use a scale, not random values.

## A scale

Define a small scale and stick to it:

```css
:root {
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
}
```

Then use only those:

```css
.card { padding: var(--space-4); }
.stack > * + * { margin-top: var(--space-4); }
.navbar { gap: var(--space-4); }
```

## Padding for inner, margin for outer

- **Padding** — inside the box, background covers it.
- **Margin** — outside, separates from neighbors.

```css
.card { padding: 1rem; } /* inside */
.card + .card { margin-top: 1rem; } /* between cards */
```

## Gap for flex and grid

Prefer `gap` over margins for flex/grid children:

```css
.row { display: flex; gap: 1rem; }
.cards { display: grid; gap: 1rem; }
```

`gap` adds space only between items, not at edges.

## Logical spacing

Use logical properties so spacing follows writing mode:

```css
.card { padding-inline: 1rem; padding-block: 0.75rem; }
.container { margin-inline: auto; }
```

## A simple stack

```css
.stack > * + * { margin-top: var(--space-4); }
```

Or with flex:

```css
.stack { display: flex; flex-direction: column; gap: var(--space-4); }
```

Both give consistent vertical rhythm.

## Recap

| Need | Use |
|------|-----|
| Scale | Define `--space-*` and reuse |
| Inner space | `padding` |
| Outer space | `margin` or `gap` |
| Rhythm | `stack` pattern or `gap` |
