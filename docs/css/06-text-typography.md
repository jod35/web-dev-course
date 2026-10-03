# Text & Typography

Good typography is mostly restraint. Pick a readable size, a comfortable line height, and stick with it.

## Base setup

```css
body {
  font-family: system-ui, -apple-system, "Segoe UI", sans-serif;
  font-size: 1rem;       /* 16px at default */
  line-height: 1.6;
  color: #1a1a1a;
}
```

`system-ui` uses the font the device already has, loads fast, and looks familiar on each OS.

## Headings

Keep them tight and bold, body text loose:

```css
h1, h2, h3 { line-height: 1.2; font-weight: 600; }
h1 { font-size: 2rem; }
h2 { font-size: 1.5rem; }
p  { margin-bottom: 1rem; }
```

Do not use headings for size. Use them for structure, then size them with CSS.

## Font stack

If you want a specific font, provide fallbacks:

```css
body { font-family: "Inter", system-ui, sans-serif; }
code { font-family: "JetBrains Mono", ui-monospace, monospace; }
```

For this course, `system-ui` is enough. Add web fonts later once layout is solid.

## Spacing for readability

```css
p { max-width: 65ch; }           /* line length you can actually read */
.lead { font-size: 1.125rem; color: #333; }
.small { font-size: 0.875rem; color: #555; }
```

`ch` is the width of a `0` character. `65ch` keeps lines from stretching across the whole screen.

## Useful properties

```css
.upper { text-transform: uppercase; letter-spacing: 0.04em; }
.muted { color: #6b7280; }
.center { text-align: center; }
.truncate {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```

## Recap

| Need | Property |
|------|----------|
| Readable body | `font-size: 1rem`, `line-height: 1.6`, `max-width: 65ch` |
| Tight headings | `line-height: 1.2` |
| Secondary text | Smaller `font-size`, muted `color` |
