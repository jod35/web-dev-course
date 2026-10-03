# Code Family

When you're writing about code, you want the markup to say "this is code", not just look monospace. HTML gives you a little family of elements for that.

## 1. Inline Code

`<code>` is for a short snippet inside a sentence:

```html
<p>
    Use the <code>print()</code> function to display text in Python.
</p>
```

Browsers typically render it in a monospace font, but the real win is semantics, tools know it's code.

---

## 2. Code Blocks

For multiple lines, pair `<pre>` with `<code>`:

```html
<pre><code>
name = "Jonathan"
print(name)
</code></pre>
```

`<pre>` keeps your spaces and line breaks exactly as typed; `<code>` says "this is code."

---

## 3. Preserving Formatting with `<pre>`

On its own, `<pre>` is the one element that respects your whitespace:

```html
<pre>
Name: Jonathan
Age: 27
Country: Uganda
</pre>
```

What you type is what you get, line breaks and indentation included.

---

## 4. What About Showing HTML Itself?

Browsers normally *interpret* tags. So this:

```html
<p>Hello World</p>
```

would render as a paragraph, not as visible code. To show the tags as text, escape them:

```html
<pre><code>
&lt;p&gt;Hello World&lt;/p&gt;
</code></pre>
```

That displays as:

```text
<p>Hello World</p>
```

Handy when you're writing tutorials (like this one!).

---

## 5. Keyboard Input

`<kbd>` marks **keys you press**:

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save the file.</p>
```

Great for instructions and shortcuts, screen readers can also announce it more meaningfully than plain text.

---

## 6. Program Output

`<samp>` is for **sample output** from a program:

```html
<p>
    The program returned:
    <samp>Hello, World!</samp>
</p>
```

It says "this is what the computer printed."

---

## 7. Variables

`<var>` marks a **variable** in maths or code:

```html
<p>The area of a rectangle is <var>width</var> × <var>height</var>.</p>
```

---

## At a glance

| Element  | When to reach for it             |
| -------- | -------------------------------- |
| `<code>` | Inline code                      |
| `<pre>`  | Preserve spaces and line breaks  |
| `<kbd>`  | Keyboard input                   |
| `<samp>` | Sample output from a program     |
| `<var>`  | A variable in an expression      |
