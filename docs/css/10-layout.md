# Layout

Layout is how boxes sit on a page. CSS gives you several layout modes, each suited to a different job.

## Normal flow

By default, block elements stack vertically, inline elements flow horizontally. This is normal flow.

```html
<h1>Title</h1>
<p>Paragraph follows block.</p>
<span>inline</span> <span>also inline</span>
```

## Positioning

- `static` — default, normal flow.
- `relative` — offset from its normal position, keeps its space:

```css
.card { position: relative; top: 0.5rem; }
```

- `absolute` — removed from flow, positioned relative to nearest positioned ancestor:

```css
.wrapper { position: relative; }
.badge { position: absolute; top: 0.5rem; right: 0.5rem; }
```

- `fixed` — relative to viewport, stays on scroll:

```css
.navbar { position: fixed; top: 0; left: 0; right: 0; }
```

- `sticky` — flow until it sticks:

```css
.toc { position: sticky; top: 1rem; }
```

## Choosing a layout mode

- A line of items, nav, button group: **Flexbox**
- Page grid, card grid: **Grid**
- Simple stacking with occasional offsets: **normal flow + positioning**
- Try flex or grid before reaching for absolute positioning.

```css
/* page skeleton: grid for outer, flex inside */
.page { display: grid; grid-template-columns: 240px 1fr; gap: 1rem; }
.navbar { display: flex; justify-content: space-between; align-items: center; }
```

## Overflow

When content does not fit:

```css
.scroller { overflow: auto; }
.no-wrap { overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
```

## Recap

| Mode | Use for |
|------|---------|
| Normal flow | Default stacking |
| Flexbox | One-dimensional distribution |
| Grid | Two-dimensional grids |
| Positioned | Overlays, sticky headers |

Pick the simplest mode that does the job.
