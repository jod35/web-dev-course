# 02,What Are Headings?

**Goal:** understand what headings **are for** before meeting all six levels.

## Headings = the document outline

Headings are **section titles**. Together they form the page's outline,the same way chapter titles outline a book:

```html
<h1>Bakery</h1>
<h2>Our Menu</h2>
```

- `<h1>` = the page's **main title**,exactly **one** per page.
- `<h2>` = major sections. `<h3>`–`<h6>` = smaller and smaller subsections.

## Meaning first, size second

Browsers draw `<h1>` biggest and `<h6>` smallest, with bold by default. But **never pick a heading for its size**:

- Need small text? Use CSS, not `<h4>`.
- Need big text? Use CSS, not `<h1>`.
- Pick the level that describes the section's **place in the outline**.


## Why headings matter beyond looks

- **Screen readers:** blind users jump between headings to navigate. Skipping `h1 → h3` confuses them,a level appears missing.
- **Search engines:** `h1`/`h2` text carries weight for what the page is about.
- **Skimmers:** most visitors scan headings before reading anything.

## Rules

1. Exactly one `<h1>` per page.
2. Never skip a level (`h1` → `h3`, `h2` → `h4`).
3. Keep headings short and descriptive.
4. Don't use headings to style non-heading text.

## Recap

| Idea | Detail |
|------|--------|
| What | Section titles forming the page outline |
| Levels | `h1` (main) → `h6` (deepest subsection) |
| Pick by | Meaning/position, never visual size |
| Matters for | Readers, screen readers, search engines |

**Next:** [03,Headings h1–h6](03-headings-showcase.md) · **Prev:** [01,Basic Structure](01-basic-structure.md)
