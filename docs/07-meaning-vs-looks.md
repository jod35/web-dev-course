# Emphasis and Meaning

HTML has several elements that make text stand out. Some describe meaning. Others only draw attention. Choosing the right one matters for screen readers, search engines, and anyone who later edits the page.

The rule: choose the element that describes the text, then use CSS if you need a different appearance.

## `<strong>` for importance

`<strong>` marks content that is important, serious, or urgent:

```html
<p><strong>Warning:</strong> The exam starts at 8am.</p>
```

Browsers usually show it in bold, but the bold is not the point. The point is that the text carries more weight than the surrounding content.

```html
<p>You <strong>must</strong> bring your student ID.</p>
```

If the text is not genuinely important, do not use `<strong>` just to make it bold.

## `<b>` for attention without importance

`<b>` draws attention without saying the text is more important:

```html
<p>The <b>MHSM Bakery</b> stall is next to the library.</p>
```

It also renders bold by default. Use it when a word needs to stand out visually but does not carry extra meaning. Many pages do not need `<b>` at all; a class and CSS often make the intent clearer.

| Element | Meaning | Default appearance |
|---------|---------|--------------------|
| `<strong>` | This content is important | Bold |
| `<b>` | Draw attention, no added importance | Bold |

## `<em>` for emphasis

`<em>` marks stress emphasis. It changes how a sentence should be read:

```html
<p>You should <em>read the question</em> before answering.</p>
```

The stress falls on "read the question". Move the emphasis and the meaning changes:

```html
<p><em>You</em> should read the question.</p>
<p>You should read <em>the question</em>.</p>
```

Browsers usually show emphasis in italics. Screen readers may also change the way they speak the word.

## `<i>` for text set apart

`<i>` marks text that is set apart by convention, without added emphasis:

```html
<p>The scientific name for the mountain gorilla is <i>Gorilla beringei beringei</i>.</p>

<p>The French word <i>bonjour</i> means hello.</p>
```

Use `<i>` for titles of works only if the title is not already marked with `<cite>`, for foreign words, technical terms, and taxonomic names. Use `<em>` when you would stress the word in speech.

| Element | Meaning | Default appearance |
|---------|---------|--------------------|
| `<em>` | Stress emphasis | Italic |
| `<i>` | Text set apart by convention | Italic |

## `<mark>` for relevance

`<mark>` highlights text that is relevant in the current context:

```html
<p>Search results for <mark>bread</mark></p>
<p>The exam will cover <mark>HTML forms</mark> and tables.</p>
```

The highlight means "this matters here", not "this is important everywhere". Do not use `<mark>` for warnings. Use `<strong>` when the text itself is important.

## Combining elements

You can combine elements when both meanings apply:

```html
<p><strong><em>Important:</em> Save your work before closing the editor.</strong></p>
```

Here `<strong>` marks the whole sentence as important, and `<em>` stresses the word "Important".

Do not stack elements to make text look more dramatic. If there is no meaning behind the markup, remove it.

## Let CSS handle appearance

You can keep the meaning and change the look:

```html
<p><strong class="warning">Warning</strong></p>
```

```css
.warning {
  color: #b00020;
  font-weight: normal;
}
```

The text is still important, even if it is not bold.

## Quick reference

| Question | Element |
|----------|---------|
| Is this important or urgent? | `<strong>` |
| Does it need vocal stress? | `<em>` |
| Should it draw the eye without added importance? | `<b>` |
| Is it a term, foreign word, or name set apart by convention? | `<i>` |
| Is it highlighted because it is relevant right now? | `<mark>` |

## Exercise: choose the element

Rewrite each sentence with the most suitable element. Be ready to explain your choice.

1. Do not share your password with anyone.
2. The word "sourdough" comes from the French word for sour.
3. Your search matched 12 results for bread.
4. The title of the book is Things Fall Apart.

One possible answer:

```html
<p><strong>Do not share your password with anyone.</strong></p>
<p>The word <i>sourdough</i> comes from the French word for sour.</p>
<p>Your search matched <mark>12 results</mark> for bread.</p>
<p>The title of the book is <cite>Things Fall Apart</cite>.</p>
```

`<cite>` is covered in the next chapters. Use it for the title of a work.

Next: [Code and Technical Text](08-code-family.md)
