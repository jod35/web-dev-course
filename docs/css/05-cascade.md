# The Cascade

When several rules target the same element, the browser picks one. That picking is the cascade.

## Source and order

Lowest priority to highest for normal rules:

1. Browser defaults
2. Your external `styles.css`
3. A `<style>` block that appears later in the document
4. Inline `style="..."`

When two rules have the same importance and specificity, the later one wins. Order in your file matters.

```css
p { color: #333; }
p { color: crimson; } /* this wins for every <p> */
```

So put general rules first, specific overrides later.

## Importance

Normal declarations vs `!important`:

```css
p { color: #333; }
p { color: crimson !important; } /* jumps ahead */
```

`!important` beats normal cascade order. Useful to override third-party CSS you cannot change, otherwise avoid it. If you need it to win against your own CSS, your selectors are probably too specific.

## Origin

User agent (browser), author (you), and user styles all participate, but for this course you only need: author styles with normal vs `!important`, and later wins when tied.

## A calm example

```css
/* base */
p { color: #333; line-height: 1.6; }

/* later in the file, same specificity, so this wins */
.lead { color: #111; font-size: 1.125rem; }
```

```html
<p class="lead">Fresh bread daily.</p>
```

No `!important`, just order and a class.

## Recap

| Concept | Remember |
|---------|---------|
| Later wins | When importance and specificity tie |
| `!important` | Beats normal cascade, use rarely |
| Keep order logical | Base first, overrides later |

Next is specificity, which decides when selectors are not tied.
