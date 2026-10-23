# Layout

Layout is about where boxes sit on the page. CSS has several layout modes, and the simplest one that works is usually the best choice.

## Normal flow

By default, block elements stack vertically and inline elements flow horizontally:

```html
<h1>Title</h1>
<p>A paragraph follows a block.</p>
<span>inline</span> <span>also inline</span>
```

This is normal flow. Most pages use it for the main document structure.

## Positioning

Positioning moves an element away from its normal place.

### `relative`

```css
.card {
  position: relative;
  top: 0.5rem;
}
```

The element is offset from its normal position, but its original space is kept.

### `absolute`

```css
.wrapper {
  position: relative;
}

.badge {
  position: absolute;
  top: 0.5rem;
  right: 0.5rem;
}
```

The element is removed from normal flow and positioned relative to its nearest positioned ancestor. In this example, the wrapper is the anchor.

### `fixed`

```css
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}
```

The element is positioned relative to the viewport and stays in place when the page scrolls.

### `sticky`

```css
.toc {
  position: sticky;
  top: 1rem;
}
```

The element behaves normally until it reaches the specified offset, then sticks.

## Choosing a layout mode

- A row of items, navigation, or a button group: Flexbox.
- A page grid or card grid: Grid.
- Simple stacking with an occasional offset: normal flow and positioning.
- Try flex or grid before reaching for absolute positioning.

```css
.page {
  display: grid;
  grid-template-columns: 240px 1fr;
  gap: 1rem;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

## Overflow

When content does not fit, decide whether it should scroll, wrap, or be clipped:

```css
.scroller {
  overflow: auto;
}

.no-wrap {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```

Avoid `overflow: hidden` on a container unless clipping is intentional. It can hide focus outlines and content.

## Try it

1. Build a page with a header, navigation, main content, and footer using normal flow.
2. Make the header a flex row with space between the title and navigation.
3. Add a badge to a card using `position: relative` on the card and `position: absolute` on the badge.
4. Make the navigation sticky at the top.
5. Resize the window and check that nothing overlaps or disappears.

If an absolutely positioned element is in the wrong place, check which ancestor is positioned.

Next: [Flexbox](11-flexbox.md)
