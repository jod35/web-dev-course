# 02 - What Are Headings?

**Goal:** In this chapter you will learn what headings **are for** before you meet all six levels.

## Headings = the document outline

Headings are **section titles**. Together they form the outline of the page, in the same way that chapter titles outline a book:

```html
<h1>Bakery</h1>
<h2>Our Menu</h2>
```

- The `<h1>` element holds the **main title** of the page, and each page contains exactly **one** `h1` element.
- The `<h2>` element marks major sections, while `<h3>` through `<h6>` mark progressively smaller subsections.

## Meaning First -  size second

Browsers draw `<h1>` as the largest heading and `<h6>` as the smallest, with bold text by default. However, you should **never select a heading for its size**:

- If you need small text, use CSS instead of `<h4>`.
- If you need large text, use CSS instead of `<h1>`.
- Select the level which describes the **position of the section in the outline**.

## Why headings matter beyond looks

- **Screen readers:** Blind users jump from heading to heading in order to navigate. When you skip from `h1` to `h3`, they encounter a missing level and lose their place.
- **Search engines:** The text in `h1` and `h2` elements carries extra weight when the search engine decides what the page is about.
- **Skimmers:** Most visitors scan the headings before they read any paragraph text.

## Rules

1. Use exactly one `<h1>` element per page.
2. Never skip a level, for example from `h1` to `h3` or from `h2` to `h4`.
3. Keep headings short and descriptive.
4. Do not use a heading to style text which is not really a heading.

## Recap

| Idea | Detail |
|------|--------|
| What | Section titles which form the page outline |
| Levels | `h1` for the main title through `h6` for the deepest subsection |
| Pick by | Meaning and position, never visual size |
| Matters for | Readers, screen readers, and search engines |

**Next:** [03 - Headings h1–h6](03-headings-showcase.md) · **Prev:** [01 - Basic Structure](01-basic-structure.md)
