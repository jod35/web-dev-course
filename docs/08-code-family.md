# 08 - Code Family

HTML provides elements for displaying **computer code, programming examples, and technical text** on a webpage.

## 1. Inline Code

The `<code>` element is used for a short piece of code within a sentence.

```html
<p>
    Use the <code>print()</code> function to display text in Python.
</p>
```

The browser normally displays `<code>` text using a monospace font.

---

## 2. Code Blocks

For multiple lines of code, `<pre>` is commonly used together with `<code>`.

```html
<pre><code>
name = "Jonathan"
print(name)
</code></pre>
```

`<pre>` preserves spaces and line breaks in the content.

---

## 3. Preserving Formatting with `<pre>`

The `<pre>` element displays text using the spacing and line breaks written in the HTML.

```html
<pre>
Name: Jonathan
Age: 27
Country: Uganda
</pre>
```

The spaces and line breaks are preserved.

---

## 4. Code with HTML

When displaying HTML code on a webpage, remember that the browser normally interprets HTML tags instead of displaying them.

For example:

```html
<p>Hello World</p>
```

To display the tags as text, you need to use HTML character references:

```html
<pre><code>
&lt;p&gt;Hello World&lt;/p&gt;
</code></pre>
```

The browser displays:

```text
<p>Hello World</p>
```

---

## 5. Keyboard Input

The `<kbd>` element represents **keyboard input**.

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save the file.</p>
```

It is useful when writing instructions involving keyboard shortcuts.

---

## 6. Program Output

The `<samp>` element represents **sample output from a computer program**.

```html
<p>
    The program returned:
    <samp>Hello, World!</samp>
</p>
```

---

## 7. Variables

The `<var>` element represents a **variable** in mathematical or programming expressions.

```html
<p>The area of a rectangle is <var>width</var> × <var>height</var>.</p>
```

---

## Important Elements

| Element  | Purpose                          |
| -------- | -------------------------------- |
| `<code>` | Represents computer code         |
| `<pre>`  | Preserves spaces and line breaks |
| `<kbd>`  | Represents keyboard input        |
| `<samp>` | Represents program output        |
| `<var>`  | Represents a variable            |
