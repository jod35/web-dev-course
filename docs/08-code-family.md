# 08 - Code Family

**Goal:** In this chapter you will learn how to mark up code, keyboard input, program output, and variables so that each one carries its own meaning.

## Tag reference

### `<code>` - code fragment

The `code` element marks inline code as code, and browsers usually render it in monospace. For multi-line blocks, wrap the element in `<pre>`, as explained in Chapter 11:

```html
<p>Run <code>print(x)</code> to debug.</p>
```

### `<kbd>` - keyboard input

The `kbd` element marks keys which the user must press. Each key belongs in its own tag:

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save.</p>
```

### `<samp>` - sample output

The `samp` element marks text which a program has produced:

```html
<p>Output: <samp>Saved.</samp></p>
```

### `<var>` - variable

The `var` element marks a mathematics or programming variable, and browsers usually render it in italic:

```html
<p><var>x</var> = 5</p>
```

The following example combines all four elements:

```html
<p>Set <var>name</var> with <code>input()</code>, press <kbd>Enter</kbd>, expect <samp>Hello!</samp></p>
```

## Rules

- The `<code>` element alone does **not** preserve line breaks. The combination `<pre><code>…</code></pre>` preserves them, as explained in Chapter 11.
- Do not use `<var>` for generic italics, because that is the job of `<i>`, or better still of `<em>`.

## Recap

| Tag | Means | Example |
|-----|-------|---------|
| `code` | Code fragment | `<code>print()</code>` |
| `kbd` | Key to press | `<kbd>Enter</kbd>` |
| `samp` | Program output | `<samp>Done.</samp>` |
| `var` | Variable | `<var>x</var>` |

**Next:** [09 - Tiny Semantics](09-tiny-semantics.md) · **Prev:** [07 - Meaning vs Looks](07-meaning-vs-looks.md)
