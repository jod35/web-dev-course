# Code and Technical Text

HTML has a small set of elements for text that is technical: code, keyboard input, program output, and variables. They are useful in tutorials, documentation, and any page that explains how something works.

## Inline code with `<code>`

Use `<code>` for a short piece of code inside a sentence:

```html
<p>Use the <code>print()</code> function to display output.</p>
```

Browsers usually show it in a monospace font. The important part is that the markup says "this is code".

## Code blocks with `<pre>` and `<code>`

For more than one line, put `<code>` inside `<pre>`:

```html
<pre><code>name = "Amina"
print(name)</code></pre>
```

`<pre>` preserves spaces and line breaks exactly as you type them. `<code>` says the content is code. Use both together for code blocks.

## Showing HTML as text

The browser treats HTML tags as markup. If you want to show a tag to the reader, escape the angle brackets:

```html
<pre><code>&lt;p&gt;Hello&lt;/p&gt;</code></pre>
```

That displays as:

```text
<p>Hello</p>
```

Use `&lt;` for `<` and `&gt;` for `>`. You will need this whenever you write about HTML itself.

## Keyboard input with `<kbd>`

`<kbd>` marks a key or key combination:

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save the file.</p>
```

It is useful in instructions. Screen readers can identify it as keyboard input rather than ordinary text.

## Program output with `<samp>`

`<samp>` marks sample output from a program:

```html
<p>The program returned:</p>
<p><samp>Hello, Amina</samp></p>
```

Use it when the text is something the computer produced.

## Variables with `<var>`

`<var>` marks a variable or placeholder in a mathematical expression or program:

```html
<p>The area of a rectangle is <var>width</var> × <var>height</var>.</p>
```

## Reference

| Element | Use | Example |
|---------|-----|---------|
| `<code>` | Inline code | `<code>print()</code>` |
| `<pre>` | Preserve whitespace | A code block or ASCII diagram |
| `<kbd>` | Keyboard input | `<kbd>Ctrl</kbd>` |
| `<samp>` | Program output | `<samp>Build complete</samp>` |
| `<var>` | Variable | `<var>total</var>` |

## Exercise: mark up a recipe tool

Create a small page that explains a command-line recipe tool. Include:

- a sentence with inline code for the command name,
- a code block with two commands,
- a sentence describing a keyboard shortcut,
- a sample output line,
- one variable in a sentence about the recipe name.

Check that the code block keeps its indentation and that the angle brackets in any HTML example appear as text rather than disappearing.

Next: [Small Semantic Tags](09-tiny-semantics.md)
