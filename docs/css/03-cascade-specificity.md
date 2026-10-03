# Cascade & Specificity

When two rules target the same element, the browser has to pick one. That picking is the cascade plus specificity plus source order.

## The cascade in one line

Lowest priority to highest:

1. Browser defaults
2. Your external `styles.css`
3. A `<style>` block later in the document
4. Inline `style="..."` — highest among normal rules

Later wins when priority is otherwise equal. That is why order in your file matters.

```css
p { color: #333; }
p { color: crimson; } /* this wins for <p> */
```

## Specificity — the score

Think of a score with three columns: `[id, class, type]`.

```css
p              → [0,0,1]
.lead          → [0,1,0]  wins over p
#intro         → [1,0,0]  wins over .lead
p.lead         → [0,1,1]  beats .lead alone
nav a:hover    → [0,1,2]
```

Higher left column beats anything on the right. An `id` beats any number of classes. That is why styling by `id` gets hard to override later.

## `!important` — use rarely

```css
p { color: crimson !important; }
```

It jumps the queue. Useful when overriding third-party CSS you cannot change, otherwise avoid it. If you use it to fix a specificity fight, you usually made the selector too specific earlier.

## Inheritance

Some properties inherit from parent to child (`color`, `font-family`, `line-height`), others do not (`margin`, `padding`, `border`). You do not need to memorize the list, just know:

```css
body {
  color: #222;
  font-family: system-ui, sans-serif;
}
```

Child paragraphs will inherit that color and font without you repeating it.

## Keeping specificity low

- Prefer classes. One class is easy to override with another class later.
- Avoid `id` selectors for styling.
- Do not nest selectors deeply. `.card p` is okay, `body main .content article .card p a` is too much.
- When you need to override, add a more specific class, do not sprinkle `!important`.

Example of a calm approach:

```css
/* base */
.btn { padding: 0.5rem 1rem; border: none; }

/* variant — just another class, not a more specific selector */
.btn-primary { background: #0a58ca; color: #fff; }
```

```html
<button class="btn btn-primary">Save</button>
```

No `!important` needed, no `id`.

## Recap

| Concept | Remember |
|---------|----------|
| Cascade | Later rule wins when specificity ties |
| Specificity | `[id, class, type]` — keep it low, prefer classes |
| Inheritance | Text styles inherit, box styles do not |
| `!important` | Escape hatch, not a habit |
