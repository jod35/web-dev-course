# Meaning vs Looks: The Core Rule

HTML has several ways to make text stand out, but they aren't interchangeable. Some tell the browser and screen reader *what the text means*; others just change how it looks. Get this distinction right and most of your other choices get easier.

> **HTML is about meaning first, looks second.**

So if something is genuinely important, you'd reach for `<strong>`. If you only want it to *look* bold without implying importance, you'd use `<b>`. Same story with `<em>` vs `<i>`. Let's see why that matters.

---

## 1. `<strong>`: strong importance

`<strong>` says the content has **real importance, seriousness or urgency**, not just "make it bold."

```html
<p>
    <strong>Warning:</strong> This action cannot be undone.
</p>
```

Yes, browsers usually render it bold. But the bold is a side effect; the meaning is the point. "Warning" deserves attention, so `<strong>` fits.

Another:

```html
<p>
    You <strong>must</strong> save your work before closing the application.
</p>
```

That "must" changes what the reader should do.

### Why we call it semantic

A semantic element describes what content *means*, not what it looks like.

```html
<strong>Important:</strong>
```

doesn't mean

> Make this text bold.

It means

> This text has strong importance.

That nuance helps with accessibility, screen readers, search engines, maintainability, and it keeps your CSS honest later on.

### Don't use `<strong>` just because you want bold

Browsers render it bold by default, but that shouldn't drive the decision:

```html
<p>
    The price is <strong>50,000 UGX</strong>.
</p>
```

If 50,000 UGX isn't actually urgent or important in context, `<strong>` is the wrong signal, even if you like the bold look. For pure styling, CSS is usually a better fit.

---

## 2. `<b>`: draw attention, no extra importance

`<b>` also looks bold by default, but it **doesn't claim the text is more important**.

```html
<p>
    Welcome to the <b>HTML Fundamentals</b> course.
</p>
```

"HTML Fundamentals" stands out visually, but we're not saying it's more important than everything else in that sentence, just noticeable.

### How `<b>` differs from `<strong>`

```html
<p>
    <strong>Warning:</strong> The server is offline.
</p>
```
→ communicates importance.

```html
<p>
    Learn <b>HTML</b>, CSS, and JavaScript.
</p>
```
→ draws the eye to "HTML" without adding importance.

Quick mental check:

| Element    | What you're saying |
| ---------- | ------------------ |
| `<strong>` | This matters a lot |
| `<b>`      | Look here, but it's not "more important" |

Both may render bold, yet they mean different things.

---

## 3. `<em>`: emphasis

`<em>` is for **emphasis** that changes how a sentence is read. Browsers usually show it italic.

```html
<p>
    You should <em>always</em> test your code.
</p>
```

"always" gets stress, it alters the intended reading.

### Emphasis can shift meaning entirely

```html
<p>
    I said you should submit the assignment.
</p>
```

Now stress different words:

```html
<p>
    <em>I</em> said you should submit the assignment.
</p>
```
→ *I* said it (not someone else).

```html
<p>
    I said <em>you</em> should submit the assignment.
</p>
```
→ *you* should do it.

```html
<p>
    I said you should <em>submit</em> the assignment.
</p>
```
→ the action matters.

That tiny italic can change interpretation, which is exactly why `<em>` carries meaning.

---

## 4. `<i>`: text set apart, not emphasized

`<i>` is for text that should be set apart from its surroundings *without* implying emphasis or importance. It also renders italic by default.

```html
<p>
    The scientific name is <i>Homo sapiens</i>.
</p>
```

Scientific names are conventionally italic.

```html
<p>
    The word <i>bonjour</i> is French.
</p>
```

Foreign words are visually differentiated, same idea.

### Not just "make it italic"

`<i>` covers things like technical terms, foreign words, taxonomic names, thoughts, or any phrase that's conventionally displayed differently. If you only want italics for decoration, CSS is usually cleaner.

---

## 5. `<em>` vs `<i>`: same look, different intent

Both go italic, but ask *why* you're marking it up.

**`<em>`: emphasis:**

```html
<p>
    You should <em>really</em> read this chapter.
</p>
```
"really" is stressed.

**`<i>`: set apart:**

```html
<p>
    The word <i>computer</i> comes from Latin roots.
</p>
```
We're presenting the term differently, not stressing it.

| Element | Purpose        | Default look |
| ------- | -------------- | ------------ |
| `<em>`  | Emphasis       | Italic       |
| `<i>`   | Text set apart | Italic       |

Looks can fool you, meaning is what splits them.

---

## 6. `<mark>`: highlighted because it's relevant right now

`<mark>` highlights text that's **relevant in the current context**. Browsers usually give it a yellowish background.

```html
<p>
    Search results for <mark>Python</mark>
</p>
```

"Python" is highlighted because it matched the search, not because it's universally important.

Other contexts:

```html
<p>
    The exam will cover <mark>HTML forms</mark> and tables.
</p>
```

```html
<p>
    Remember to bring your <mark>student ID</mark> to the examination.
</p>
```

In each case, you're drawing the reader's eye to what's pertinent *here and now*.

---

## 7. Quick contrasts you'll actually use

### `<mark>` vs `<strong>`

- `<strong>` → *"This is important."* E.g. `<strong>Do not share your password.</strong>`
- `<mark>` → *"This is relevant/highlighted here."* E.g. `Your search found <mark>25 results</mark>.`

Highlighting isn't importance; importance isn't just highlighting.

### `<strong>` vs `<b>`

```html
<p>
    <strong>Warning:</strong> Your account will be deleted.
</p>
```
That's urgent, `<strong>`.

```html
<p>
    Learn <b>Python</b> with practical projects.
</p>
```
That's visually distinct, `<b>`.

Rule of thumb:
- Importance → `<strong>`, eye-catcher without importance → `<b>`.

### `<em>` vs `<i>`

```html
<p>
    You should <em>carefully</em> read the instructions.
</p>
```
Emphasis → `<em>`.

```html
<p>
    The French word <i>bonjour</i> means hello.
</p>
```
Set apart → `<i>`.

Rule of thumb:
- Want vocal stress? `<em>`. Need a different voice or convention? `<i>`.

---

## 8. You Can Combine Them: Sparingly

When both meanings really apply, nesting is fine:

```html
<p>
    <strong>
        <em>Important:</em>
        Save your work before continuing.
    </strong>
</p>
```
`<strong>` = important. `<em>` = emphasis on "Important".

Highlight plus importance is also okay when both are true:

```html
<p>
    <mark><strong>Deadline: Friday</strong></mark>
</p>
```

Just don't stack them to make text look "more dramatic." If there's no meaning behind it, leave it out.

---

## 9. Appearance Isn't the Point

By default you'll see:

```html
<strong>Important</strong>
<b>Bold</b>
<em>Emphasized</em>
<i>Italic</i>
<mark>Highlighted</mark>
```

Roughly:

* `<strong>` → **bold**
* `<b>` → **bold**
* `<em>` → *italic*
* `<i>` → *italic*
* `<mark>` → highlighted background

So `<strong>` and `<b>` *can* look identical, same for `<em>`/`<i>`. That's exactly why you shouldn't choose based on looks.

---

## 10. Let CSS Handle Looks

HTML says what something *is*; CSS decides how it *looks*. So you can keep the meaning and change the presentation:

```html
<strong class="warning">Warning</strong>
```
```css
.warning {
    color: red;
    font-weight: normal;
}
```
It's still "strong importance," even if it's no longer bold.

Likewise, you can make normal text look bold without `<b>`:

```html
<p class="important">Important information</p>
```
```css
.important {
    font-weight: bold;
}
```

Separating meaning from appearance is the habit that scales.

---

## 11. Common Mix-Ups

**"I want bold, so `<b>` everywhere."**
If "Warning" is actually important, prefer `<strong>Warning</strong>`.

**"I want italic, so `<i>` everywhere."**
If you mean vocal emphasis, `You *must* read this`, use `<em>You must read this carefully.</em>`.

**"My favourite language is Python: I'll just strong it."**
```html
<p>
    My favorite language is <strong>Python</strong>.
</p>
```
If "Python" isn't especially important in context, bolding it with `<strong>` muddies the signal. Consider `<b>` or CSS.

**"`<mark>` for warnings."**
```html
<mark>WARNING: Do not delete this file.</mark>
```
That's importance, not highlighting. Reach for `<strong>` (and add `<mark>` only if highlighting is also relevant).

---

## 12. Putting It All Together

```html
<p>
    <strong>Important:</strong>
    You should <em>always</em> back up your files.
    The term <i>backup</i> refers to an additional copy of your data.
    <mark>Remember to test your backups.</mark>
</p>
```

- `<strong>Important:</strong>`: strong importance.
- `<em>always</em>`: vocal emphasis.
- `<i>backup</i>`: term set apart.
- `<mark>Remember to test your backups.</mark>`: relevant and worth highlighting now.

Each choice signals something a browser or screen reader can actually use.

---

## 13. Quick Reference

| Element    | Meaning                            | Typical look       | Reach for it when |
| ---------- | ---------------------------------- | ------------------ | ----------------- |
| `<strong>` | Strong importance                  | **Bold**           | Something is important or urgent |
| `<b>`      | Attention without added importance | **Bold**           | You need visual distinction but no extra semantics |
| `<em>`     | Emphasis                           | *Italic*           | You'd stress the word when speaking |
| `<i>`      | Text set apart                     | *Italic*           | Term needs a different voice or convention |
| `<mark>`   | Highlighted relevance              | Highlighted        | It's relevant or noteworthy *in this context* |

---

## 14. The Main Idea

Don't pick these tags by how they render. Ask what the text *means*:

```text
Is it important or urgent?
        ↓
    <strong>

Does it need vocal stress?
        ↓
       <em>

Just need to draw the eye without implying importance?
        ↓
        <b>

Is it a term or phrase set apart by convention?
        ↓
        <i>

Is it being highlighted because it's relevant right now?
        ↓
      <mark>
```

The browser's default styling is just a starting point. **Semantic HTML describes what your content is; CSS can decide how it looks.**
