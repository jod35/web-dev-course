# Combined: Headings + Paragraphs in the Basic Structure

Headings and paragraphs do the heavy lifting for text on most pages. A **heading** names the section, a **paragraph** says something about it. The trick is using them together so the document actually makes sense.

---

## 1. A Heading Followed by a Paragraph

The simplest combo:

```html
<h1>Learning HTML</h1>

<p>
    HTML is the language used to structure content on the web.
</p>
```

Here:

* `<h1>` names the topic.
* `<p>` gives you the detail.

Browsers will render the heading bigger and bolder and put the paragraph underneath — but you're choosing them for meaning, not just looks.

---

## 2. Multiple Paragraphs Under One Heading

One heading can comfortably introduce several paragraphs:

```html
<h1>Learning HTML</h1>

<p>
    HTML is used to structure content on webpages.
</p>

<p>
    It provides elements for headings, paragraphs, links,
    images, tables, forms, and many other types of content.
</p>
```

Both paragraphs sit under that `<h1>`. When you feel yourself starting a new idea or point, that's your cue for a new `<p>` — don't cram everything into one long block.

---

## 3. Using Different Heading Levels

Six levels are available:

```html
<h1>...</h1>
<h2>...</h2>
<h3>...</h3>
<h4>...</h4>
<h5>...</h5>
<h6>...</h6>
```

They signal how deep you are in the outline. For instance:

```html
<h1>Web Development</h1>

<p>
    Web development involves creating websites and web applications.
</p>

<h2>HTML</h2>

<p>
    HTML is used to structure the content of a webpage.
</p>

<h2>CSS</h2>

<p>
    CSS is used to control the appearance of a webpage.
</p>

<h2>JavaScript</h2>

<p>
    JavaScript is used to add behaviour and interactivity.
</p>
```

Visualised:

```text
Web Development
│
├── HTML
│
├── CSS
│
└── JavaScript
```

`<h1>` is the main topic; each `<h2>` is a major section inside it.

---

## 4. Adding Subsections

You can nest sections further:

```html
<h1>Web Development</h1>

<p>
    Web development involves building websites and web applications.
</p>

<h2>Frontend Development</h2>

<p>
    Frontend development focuses on the parts of a website that users
    see and interact with.
</p>

<h3>HTML</h3>

<p>
    HTML provides the structure of the webpage.
</p>

<h3>CSS</h3>

<p>
    CSS controls the appearance of the webpage.
</p>

<h2>Backend Development</h2>

<p>
    Backend development deals with servers, databases, APIs, and
    application logic.
</p>
```

Hierarchy:

```text
Web Development              <h1>
│
├── Frontend Development     <h2>
│   │
│   ├── HTML                 <h3>
│   │
│   └── CSS                  <h3>
│
└── Backend Development      <h2>
```

Heading levels are how you communicate that nesting to browsers and assistive tech.

---

## 5. A Heading Should Say What Comes Next

Make it descriptive. Compare:

Good:

```html
<h2>HTML Tables</h2>

<p>
    HTML tables allow us to organize information into rows and columns.
</p>
```

Also good:

```html
<h2>Creating Links</h2>

<p>
    The anchor element is used to create hyperlinks between webpages.
</p>
```

In both cases the reader knows immediately what the paragraph will cover. If your heading could sit above any paragraph, it's probably too vague.

---

## 6. Don't Use Headings Just to Make Text Bigger

It's a common slip — we like how `<h2>` looks, so we wrap any large text in it:

```html
<h2>Welcome to my website</h2>
```

If that's just a normal line you want styled large, it shouldn't be a heading. Headings are for **document structure**. Let CSS handle looks:

```html
<p class="large-text">Welcome to my website</p>
```

```css
.large-text {
    font-size: 2rem;
}
```

---

## 7. Don't Skip Levels for Appearance

This jumps over `<h2>`:

```html
<h1>Web Development</h1>

<h3>HTML</h3>
```

Stick to the logical order instead:

```html
<h1>Web Development</h1>

<h2>HTML</h2>
```

And if HTML itself has sub-topics:

```html
<h1>Web Development</h1>

<h2>HTML</h2>

<h3>Elements</h3>

<h3>Attributes</h3>

<h3>Forms</h3>
```

It's about **hierarchy that makes sense**, not making each heading a little smaller.

---

## 8. One `<h1>` for the Main Topic

For a simple page:

```html
<h1>Introduction to Python</h1>

<p>
    Python is a general-purpose programming language known for its
    readable syntax.
</p>

<h2>Variables</h2>

<p>
    Variables allow us to store and work with values in a program.
</p>

<h2>Functions</h2>

<p>
    Functions allow us to organize reusable pieces of code.
</p>

<h2>Classes</h2>

<p>
    Classes provide a way to model objects and organize related data
    and behaviour.
</p>
```

Think of `<h1>` as the document title; `<h2>`s divide that title into sections.

---

## 9. Headings and Paragraphs Build the Whole Document

You'll reuse this pattern everywhere:

```html
<h1>Main Topic</h1>

<p>Introduction to the main topic.</p>

<h2>First Section</h2>

<p>Information about the first section.</p>

<p>More information about the first section.</p>

<h2>Second Section</h2>

<p>Information about the second section.</p>

<h3>Subsection</h3>

<p>More specific information about the second section.</p>
```

That repetition is a feature — once you see it, pages become easier to skim, and browsers, search engines and screen readers can build a better map of your content.

---

## 10. A Real-World Example — Uganda

Say you're putting together a quick info page:

```html
<h1>Uganda</h1>

<p>
    Uganda is a country in East Africa known for its diverse landscapes,
    wildlife, and cultures.
</p>

<h2>Geography</h2>

<p>
    Uganda is located in East Africa and has a landscape that includes
    lakes, mountains, forests, and savannahs.
</p>

<h2>Wildlife</h2>

<p>
    Uganda is home to many species of wildlife, including elephants,
    lions, chimpanzees, and mountain gorillas.
</p>

<h3>Mountain Gorillas</h3>

<p>
    Mountain gorillas can be found in the forests of southwestern Uganda.
</p>

<h2>Culture</h2>

<p>
    Uganda has many different cultural groups, languages, traditions,
    and forms of artistic expression.
</p>
```

Structure:

```text
Uganda
│
├── Geography
│
├── Wildlife
│   │
│   └── Mountain Gorillas
│
└── Culture
```

You're not just displaying text — you're describing how the pieces relate.

---

## Quick Rule of Thumb

Ask yourself:

**Heading → What is this section about?**

**Paragraph → What do I want to say about it?**

E.g.:

```html
<h2>HTML Forms</h2>

<p>
    HTML forms allow users to enter and submit information to a website.
</p>
```

Heading names it; paragraph explains it.
