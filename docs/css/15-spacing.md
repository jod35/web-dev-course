# Spacing

Spacing makes a page readable. Use a small scale instead of choosing a new value for every gap.

## A spacing scale

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

Then use only those values:

```css
.card {
  padding: var(--space-4);
}

.stack > * + * {
  margin-top: var(--space-4);
}

.navbar {
  gap: var(--space-4);
}
```

A scale keeps spacing consistent and makes it easy to adjust the whole page later.

## Padding, margin, and gap

- **Padding** is space inside a box. The background covers it.
- **Margin** is space outside a box. It separates the box from its neighbours.
- **Gap** adds space between children in flex or grid layout.

```css
.card {
  padding: 1rem;
}

.card + .card {
  margin-top: 1rem;
}

.row {
  display: flex;
  gap: 1rem;
}
```

Prefer `gap` over margins for flex and grid children. It adds space only between items, not at the edges.

## Logical spacing

Logical properties follow the writing direction:

```css
.card {
  padding-inline: 1rem;
  padding-block: 0.75rem;
}

.container {
  margin-inline: auto;
}
```

Use them when the page may be translated or displayed in a different writing mode.

## A simple stack

```css
.stack > * + * {
  margin-top: var(--space-4);
}
```

Or with flexbox:

```css
.stack {
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
}
```

Both create consistent vertical rhythm. The flex version avoids margin collapse.

## Try it

1. Define a spacing scale with four values.
2. Use it for card padding, a stack of paragraphs, and a flex row.
3. Change the middle value and see which parts of the page move.
4. Replace one margin with `gap` in a flex container.
5. Make the window narrow and check that the spacing still looks reasonable.

If the gaps look uneven, check whether some elements still have default margins.

Next: [Pseudo-elements](16-pseudo-elements.md)
