# Typography

Readable typography is mostly restraint: a comfortable size, a sensible line length, and enough line height.

## Base text

```css
body {
  font-family: system-ui, -apple-system, "Segoe UI", sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  color: #1a1a1a;
}
```

`system-ui` uses the font already installed on the device. It loads quickly and looks familiar on each operating system.

## Headings

Keep headings tight and body text more open:

```css
h1,
h2,
h3 {
  line-height: 1.2;
  font-weight: 600;
}

h1 {
  font-size: 2rem;
}

h2 {
  font-size: 1.5rem;
}

p {
  margin-bottom: 1rem;
}
```

Use heading elements for structure. Use CSS to change their size.

## Font stacks

If you use a web font, provide fallbacks:

```css
body {
  font-family: "Inter", system-ui, sans-serif;
}

code {
  font-family: "JetBrains Mono", ui-monospace, monospace;
}
```

For this course, `system-ui` is enough. Add a web font after the layout and content are working.

## Line length

```css
p {
  max-width: 65ch;
}
```

`ch` is roughly the width of the `0` character. A line around 60 to 75 characters is comfortable to read. Without a maximum width, text stretches across wide screens and becomes hard to follow.

## Useful properties

```css
.upper {
  text-transform: uppercase;
  letter-spacing: 0.04em;
}

.muted {
  color: #6b7280;
}

.center {
  text-align: center;
}

.truncate {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```

Use uppercase sparingly. It is harder to read in long passages, and `letter-spacing` helps only a little.

## Try it

1. Set a base font family, size, line height, and colour on `body`.
2. Set a maximum width of `65ch` on paragraphs.
3. Style `h1`, `h2`, and `h3` with a tighter line height.
4. Make one paragraph larger with a class, without changing its heading level.
5. Resize the browser and check that the text remains readable at a narrow width.

If long lines are hard to read, add a maximum width to the text container.

Next: [Responsive](21-responsive.md)
