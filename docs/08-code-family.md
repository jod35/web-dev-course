# 08 - Code Family

**Goal:** mark up code, keyboard input, program output, and variables with meaning.

## Tag reference

### `<code>` - code fragment

Inline code with code meaning (usually monospace). For multi-line blocks, wrap in `<pre>` (Chapter 11):

```html
<p>Run <code>print(x)</code> to debug.</p>
```

### `<kbd>` - keyboard input

Keys the user must press. Put **each key** in its own tag:

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save.</p>
```

### `<samp>` - sample output

Text a program produced:

```html
<p>Output: <samp>Saved.</samp></p>
```

### `<var>` - variable

A math or programming variable (usually italic):

```html
<p><var>x</var> = 5</p>
```

Combined example:

```html
<p>Set <var>name</var> with <code>input()</code>, press <kbd>Enter</kbd>, expect <samp>Hello!</samp></p>
```

## Rules

- `<code>` alone does **not** preserve line breaks,`<pre><code>…</code></pre>` does (see Chapter 11).
- Don't use `<var>` for generic italics,that is `<i>` (or better, `<em>`).

## Recap

| Tag | Means | Example |
|-----|-------|---------|
| `code` | Code fragment | `<code>print()</code>` |
| `kbd` | Key to press | `<kbd>Enter</kbd>` |
| `samp` | Program output | `<samp>Done.</samp>` |
| `var` | Variable | `<var>x</var>` |

**Next:** [09 - Tiny Semantics](09-tiny-semantics.md) · **Prev:** [07 - Meaning vs Looks](07-meaning-vs-looks.md)
