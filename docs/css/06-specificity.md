# Specificity

Specificity is the score that decides which selector wins when cascade order alone is not enough.

## The score

Three columns: `[id, class, type]`.

```css
p              → [0,0,1]
.lead          → [0,1,0]  wins over p
p.lead         → [0,1,1]  beats .lead alone
#intro         → [1,0,0]  wins over any number of classes
nav a:hover    → [0,1,2]
```

Left column beats everything to its right. One `id` beats any number of classes, so styling by `id` gets hard to override later.

## Keeping it low

- Prefer classes. One class is easy to override with another class.
- Avoid `id` selectors for styling.
- Do not nest selectors deeply. `.card p` is fine, `body main .content article .card p a` is too much.
- To override, add another class, not `!important`.

```css
/* base */
.btn { padding: 0.5rem 1rem; border: none; }

/* variant, just another class, same specificity, later wins */
.btn-primary { background: #0a58ca; color: #fff; }
```

```html
<button class="btn btn-primary">Save</button>
```

No `!important`, no `id`.

## Where people slip

```css
/* too specific from the start */
#header nav ul li a { color: crimson; }

/* now you need even more specificity to change it */
```

Instead:

```css
.nav-link { color: crimson; }
.nav-link:hover { color: #a00; }
```

Short, flat, easy to reason about.

## Recap

| Selector | Score | Advice |
|----------|-------|--------|
| `p` | [0,0,1] | Base defaults |
| `.lead`, `:hover`, `[type="email"]` | [0,1,0] | Most styling |
| `#header` | [1,0,0] | Avoid for styling |
