# Meaning vs Looks (The Core Rule)

HTML provides several elements for making text **stand out**. Some of these elements communicate meaning to the browser and assistive technologies, while others are mainly used to change the visual appearance of text.

The most important distinction to understand is:

> **HTML is about meaning, not just appearance.**

For example, if you want to tell the browser that certain words are important, use `<strong>`. If you only want text to *look* bold without giving it additional importance, use `<b>`.

The same idea applies to `<em>` and `<i>`.

---

## 1. The `<strong>` Element

The `<strong>` element indicates that the content has **strong importance, seriousness, or urgency**.

### Basic example

```html
<p>
    <strong>Warning:</strong> This action cannot be undone.
</p>
```

The browser normally displays the text inside `<strong>` in **bold**.

However, the important part is not the bold appearance. The important part is the **meaning**.

The word "Warning" is important to the reader, so `<strong>` is appropriate.

### Another example

```html
<p>
    You <strong>must</strong> save your work before closing the application.
</p>
```

Here, "must" is strongly important to the meaning of the sentence.

---

### `<strong>` is semantic

A semantic element tells us what the content **means**.

For example:

```html
<strong>Important:</strong>
```

does not simply mean:

> Make this text bold.

It means:

> This text has strong importance.

This distinction becomes particularly useful for:

* accessibility
* screen readers
* search engines
* maintaining understandable HTML
* styling content with CSS later

---

### `<strong>` does not mean "make it bold"

Although browsers usually render `<strong>` as bold text, you should not choose it simply because you want bold text.

For example:

```html
<p>
    The price is <strong>50,000 UGX</strong>.
</p>
```

If the price is not particularly important or urgent, `<strong>` may not be the best choice simply because you want it to appear bold.

If you only want a visual effect, CSS is often more appropriate.

---

## 2. The `<b>` Element

The `<b>` element is used to draw attention to text **without saying that the text has increased importance**.

By default, browsers display `<b>` as bold.

### Example

```html
<p>
    Welcome to the <b>HTML Fundamentals</b> course.
</p>
```

The words "HTML Fundamentals" are visually noticeable, but they are not necessarily more important than the rest of the sentence.

---

### `<b>` is not the same as `<strong>`

Compare these examples:

```html
<p>
    <strong>Warning:</strong> The server is offline.
</p>
```

and:

```html
<p>
    Learn <b>HTML</b>, CSS, and JavaScript.
</p>
```

The first example communicates **importance**.

The second example simply draws attention to the word "HTML".

### Think of it this way

| Element    | Meaning                        |
| ---------- | ------------------------------ |
| `<strong>` | This content is important      |
| `<b>`      | Draw attention to this content |

Both may appear bold, but they communicate different things.

---

## 3. The `<em>` Element

The `<em>` element represents **emphasis**.

Browsers normally display emphasized text in *italics*.

### Example

```html
<p>
    You should <em>always</em> test your code.
</p>
```

The word "always" is emphasized because it changes how the sentence should be understood.

---

### `<em>` can change the meaning of a sentence

Consider:

```html
<p>
    I said you should submit the assignment.
</p>
```

Now emphasize different words:

```html
<p>
    <em>I</em> said you should submit the assignment.
</p>
```

This emphasizes who said it.

```html
<p>
    I said <em>you</em> should submit the assignment.
</p>
```

This emphasizes who should submit it.

```html
<p>
    I said you should <em>submit</em> the assignment.
</p>
```

This emphasizes the action.

The emphasis can therefore affect how the sentence is interpreted.

---

## 4. The `<i>` Element

The `<i>` element represents text that is set apart from the surrounding content for a particular reason, without conveying the importance that `<strong>` or emphasis that `<em>` conveys.

Browsers normally display `<i>` as *italic text*.

### Example

```html
<p>
    The scientific name is <i>Homo sapiens</i>.
</p>
```

Here, italics are commonly used for the scientific name.

Another example:

```html
<p>
    The word <i>bonjour</i> is French.
</p>
```

The French word is visually differentiated from the surrounding English text.

---

### `<i>` is not simply "make text italic"

Although `<i>` normally produces italic text, its semantic purpose is broader than simply changing the font style.

It can be used for content such as:

* technical terms
* foreign words
* taxonomic names
* thoughts
* terms that are conventionally displayed differently
* other text that needs to be set apart from the surrounding content

If you simply want to make something italic for visual reasons, CSS is generally a better choice.

---

## 5. `<em>` vs `<i>`

These two elements are often confused because both normally appear italic.

The difference is **meaning**.

### `<em>`

Use `<em>` when the text should receive **emphasis**.

```html
<p>
    You should <em>really</em> read this chapter.
</p>
```

The word "really" is emphasized.

### `<i>`

Use `<i>` when the text needs to be **set apart from the surrounding text**, but is not necessarily emphasized.

```html
<p>
    The word <i>computer</i> comes from Latin roots.
</p>
```

The word is being presented differently, rather than emphasized as particularly important.

### Comparison

| Element | Purpose        | Default appearance |
| ------- | -------------- | ------------------ |
| `<em>`  | Emphasis       | Italic             |
| `<i>`   | Text set apart | Italic             |

Again, the appearance is similar, but the meaning is different.

---

## 6. The `<mark>` Element

The `<mark>` element represents text that is **highlighted or marked because it is relevant in the current context**.

Browsers normally display `<mark>` with a highlighted background.

### Example

```html
<p>
    Search results for <mark>Python</mark>
</p>
```

The word "Python" has been highlighted because it matches what the user searched for.

---

### Highlighting a passage

You can use `<mark>` to draw attention to a particular part of a sentence.

```html
<p>
    The exam will cover <mark>HTML forms</mark> and tables.
</p>
```

The highlighted text is relevant to the reader.

Another example:

```html
<p>
    Remember to bring your <mark>student ID</mark> to the examination.
</p>
```

The phrase "student ID" is highlighted to draw the reader's attention to it.

---

## 7. `<mark>` vs `<strong>`

These elements can both make something stand out, but they communicate different ideas.

### `<strong>`

Means:

> This content is important.

```html
<p>
    <strong>Do not share your password.</strong>
</p>
```

### `<mark>`

Means:

> This part is being highlighted because it is relevant or noteworthy in this context.

```html
<p>
    Your search found <mark>25 results</mark>.
</p>
```

The result count is highlighted, but that does not necessarily mean it is inherently important.

---

## 8. `<strong>` vs `<b>`

Consider:

```html
<p>
    <strong>Warning:</strong> Your account will be deleted.
</p>
```

The warning has strong importance.

Now consider:

```html
<p>
    Learn <b>Python</b> with practical projects.
</p>
```

The word "Python" is simply being visually distinguished.

### Quick rule

Use:

```html
<strong>
```

when the **meaning is importance**.

Use:

```html
<b>
```

when you want to **draw attention without adding importance**.

---

## 9. `<em>` vs `<i>`

Similarly:

```html
<p>
    You should <em>carefully</em> read the instructions.
</p>
```

The word "carefully" is emphasized.

Whereas:

```html
<p>
    The French word <i>bonjour</i> means hello.
</p>
```

The foreign word is set apart from the surrounding text.

### Quick rule

Use:

```html
<em>
```

when the **meaning involves emphasis**.

Use:

```html
<i>
```

when the text is **set apart without emphasis**.

---

## 10. Combining These Elements

These elements can be nested when their meanings genuinely apply.

For example:

```html
<p>
    <strong>
        <em>Important:</em>
        Save your work before continuing.
    </strong>
</p>
```

Here:

* `<strong>` communicates importance.
* `<em>` gives emphasis to the word "Important".

You can also combine highlighting with importance:

```html
<p>
    <mark><strong>Deadline: Friday</strong></mark>
</p>
```

However, don't combine elements simply to make text look more dramatic. Each element should have a meaningful purpose.

---

## 11. Appearance Is Not the Main Point

By default, browsers generally render these elements like this:

```html
<strong>Important</strong>
<b>Bold</b>
<em>Emphasized</em>
<i>Italic</i>
<mark>Highlighted</mark>
```

The visual result is approximately:

* `<strong>` → **bold**
* `<b>` → **bold**
* `<em>` → *italic*
* `<i>` → *italic*
* `<mark>` → highlighted background

This can make `<strong>` and `<b>` appear identical, and `<em>` and `<i>` appear identical.

But they are **not semantically identical**.

---

## 12. CSS Controls Appearance

HTML communicates structure and meaning. CSS controls presentation.

For example, you can change how `<strong>` looks:

```html
<strong class="warning">Warning</strong>
```

```css
.warning {
    color: red;
    font-weight: normal;
}
```

The `<strong>` element still communicates importance even though it is no longer visually bold.

Similarly, you can make something look bold without using `<b>`:

```html
<p class="important">Important information</p>
```

```css
.important {
    font-weight: bold;
}
```

This is useful because it separates **meaning** from **appearance**.

---

## 13. Common Mistakes

### Mistake 1: Using `<b>` for everything that should be bold

```html
<b>Warning</b>
```

If "Warning" is actually important, use:

```html
<strong>Warning</strong>
```

---

### Mistake 2: Using `<i>` for every italicized word

```html
<i>You must read this carefully.</i>
```

If the purpose is emphasis, use:

```html
<em>You must read this carefully.</em>
```

---

### Mistake 3: Using `<strong>` just for styling

```html
<p>
    My favorite language is <strong>Python</strong>.
</p>
```

If "Python" is not especially important, using `<strong>` purely to make it bold is not ideal.

Consider CSS or `<b>` depending on the intended meaning.

---

### Mistake 4: Using `<mark>` as a replacement for `<strong>`

```html
<mark>WARNING: Do not delete this file.</mark>
```

Highlighting and importance are different concepts.

If the purpose is to communicate strong importance:

```html
<strong>WARNING: Do not delete this file.</strong>
```

If you also want the text highlighted because it is particularly relevant in the current context, then `<mark>` may be appropriate as well.

---

## 14. A Practical Example

Consider this paragraph:

```html
<p>
    <strong>Important:</strong>
    You should <em>always</em> back up your files.
    The term <i>backup</i> refers to an additional copy of your data.
    <mark>Remember to test your backups.</mark>
</p>
```

Each element has a different purpose:

### `<strong>`

```html
<strong>Important:</strong>
```

Communicates strong importance.

### `<em>`

```html
<em>always</em>
```

Emphasizes the word "always".

### `<i>`

```html
<i>backup</i>
```

Sets the term apart from the surrounding text.

### `<mark>`

```html
<mark>Remember to test your backups.</mark>
```

Highlights information that is relevant to the reader.

---

## 15. Quick Reference

| Element    | Meaning                            | Typical appearance | Use it when                                             |
| ---------- | ---------------------------------- | ------------------ | ------------------------------------------------------- |
| `<strong>` | Strong importance                  | **Bold**           | Content is important or urgent                          |
| `<b>`      | Attention without added importance | **Bold**           | You need visual distinction without semantic importance |
| `<em>`     | Emphasis                           | *Italic*           | You want to emphasize the meaning of the text           |
| `<i>`      | Text set apart                     | *Italic*           | Text needs a different voice or context                 |
| `<mark>`   | Highlighted relevance              | Highlighted        | Text is relevant or noteworthy in the current context   |

---

## 16. The Main Idea

Do not choose these elements based only on what they **look like**.

Instead, ask what the text **means**.

```text
Is it important?
        ↓
    <strong>

Does it need emphasis?
        ↓
      <em>

Does it simply need to be visually distinguished?
        ↓
       <b>

Is it being set apart from the surrounding text?
        ↓
       <i>

Does it need to be highlighted as relevant?
        ↓
     <mark>
```

The browser's default styling is only the starting point. **Semantic HTML describes the meaning of your content, while CSS can control how that content looks.**
