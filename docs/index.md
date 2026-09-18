---
icon: lucide/house
---

# Intro to HTML - What HTML Is

**Goal:** In this chapter you will learn what HTML is, what it does, and how you write and save it before you create your first page.

## What is HTML?

**HTML stands for HyperText Markup Language.**

- **HyperText** refers to text that can link to other text. A HyperText page can point to another page through links.
- **Markup** means that you mark up plain text with labels which describe what each part is.
- **Language** means that HTML provides a fixed set of labels, called *tags*, which every browser understands.

HTML is **not a programming language**. It has no logic, no variables, and no `if` statements. It is a **markup language** because it describes the structure and meaning of content.

## What does HTML do?

HTML tells the browser **what things are**, not what they look like.

```html
<h1>Bakery</h1>
<p>Fresh bread daily.</p>
```

- The line `<h1>Bakery</h1>` means that the text is the main title of the page.
- The line `<p>Fresh bread daily.</p>` means that the text is a paragraph.

The browser then decides how to display that meaning with a large bold title and a plain paragraph. The exact colours, fonts, and layout are added later with **CSS**. Behaviour and interactivity are added later with **JavaScript**.

| Technology | Job | Example |
|------------|-----|---------|
| **HTML** | Structure and meaning | "This is a heading, this is a paragraph, this is a link." |
| **CSS** | Looks and layout | "Make the heading red and centred." |
| **JavaScript** | Behaviour | "When clicked, show the menu." |

This course covers **HTML only**. One core rule applies throughout the course: **choose tags by meaning, never by looks.**

## Tags vs elements

Beginners often mix up these two terms, but they describe different things:

- A **tag** is the label inside angle brackets, for example `<p>`, `</p>`, or `<h1>`.
- An **element** is the complete unit, which consists of the opening tag, the content, and the closing tag.

<figure markdown="span">

![Image title](./imgs/opening_tag.png){ width="300" }

<figcaption>An opening tag</figcaption>

</figure>

<figure markdown="span">

![Image title](./imgs/closing_tag.png){ width="300" }

<figcaption>A closing tag</figcaption>

</figure>

Most elements have both an opening tag and a closing tag:

```html
<h1>Bakery</h1>      <!-- opening <h1>, text, closing </h1> -->
<p>Fresh bread.</p>  <!-- opening <p>, text, closing </p> -->
```

A few elements have **no content and no closing tag**. These elements are called **void (empty) elements**:

```html
<br>   <!-- line break -->
<hr>   <!-- horizontal rule -->
<img src="bread.jpg" alt="Loaf of bread">  <!-- image -->
```

## Attributes

Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and they consist of two parts, a name and a value, which are separated by an equals sign.

<figure markdown="span">

![Image title](./imgs/attributes.png){ width="300" }

<figcaption>HTML Attributes</figcaption>

</figure>

!!! note "The pattern to notice"
    Opening tags can carry extra information in the form of **attributes**, such as `src` and `alt` in the example above. Closing tags never carry attributes. You will meet each attribute in its own chapter, so for now it is enough to recognise the general shape.

## How HTML is stored, written, and saved

1. **HTML is plain text.** No special software creates it. It consists of ordinary characters stored in a file.
2. **You write HTML in a text editor** such as VS Code, Notepad, or TextEdit, which are all programs that save plain text. Do **not** use Word or Google Docs because they add hidden formatting which breaks HTML.
3. **You save the file with an `.html` ending**, for example `index.html`. The `.html` ending tells the operating system and the browser that the file should be read as a webpage.
4. **You open the file in a browser** by double-clicking it or by dragging it into Chrome, Firefox, or Edge. The browser reads the file from top to bottom and draws the page.

Practical rules for this course:

- Save every exercise as `index.html` inside its own folder.
- Always use **UTF-8 encoding**, which is the default in most editors. UTF-8 keeps characters such as `é`, `ñ`, and `ü` intact.
- Name files in **lowercase without spaces**, for example `index.html` instead of `My Page.HTML`.
- After every change, **save the file and then refresh the browser**. If you do not save, the change will not appear on the screen.

You do not need a server, the internet, or any build tool yet. A text file and a browser provide the complete setup.

## Try it: your first 3 lines

1. Open your editor and create a new file.
2. Type exactly this:

```html
<h1>Bakery</h1>
<p>Fresh bread daily.</p>
```

3. Save the file as `index.html`.
4. Open the file in a browser.

You have just written HTML with two elements, four tags, one title, and one paragraph. Every later chapter introduces more labels for more kinds of content.

## Recap

| Idea | Detail |
|------|--------|
| What HTML is | HyperText Markup Language, a set of labels for structure and meaning |
| What it does | It states what content *is*; the browser renders it, CSS controls looks, and JS controls behaviour |
| Tag | The bracketed label, for example `<p>` or `</p>` |
| Element | The complete unit, which is the opening tag plus the content plus the closing tag, or a lone void element such as `<br>` |
| How it lives | A plain-text `.html` file which is written in a code editor and opened in a browser |

**Next:** [Course Index](00-index.md), which explains how the course is organised, then [01 - Basic Structure](01-basic-structure.md).
