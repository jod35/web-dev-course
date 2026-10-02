# Combined: Headings + Paragraphs in the Basic Structure

Headings and paragraphs are two of the most common elements used to organize text on a webpage.

A **heading** introduces a topic or section, while a **paragraph** contains the information that explains that topic.

The key idea is to use them together to create a clear document structure.

---

## 1. A Heading Followed by a Paragraph

The most basic combination is a heading followed by one or more paragraphs.

```html
<h1>Learning HTML</h1>

<p>
    HTML is the language used to structure content on the web.
</p>
```

Here:

* `<h1>` introduces the main topic.
* `<p>` provides information about that topic.

The browser normally displays the heading in a larger, bold font and places the paragraph underneath it.

---

## 2. Multiple Paragraphs Under One Heading

A heading can introduce several paragraphs.

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

Both paragraphs belong to the topic introduced by the heading.

You should create a new paragraph when you are starting a new **idea or point**, rather than putting everything into one large paragraph.

---

## 3. Using Different Heading Levels

HTML provides six heading levels:

```html
<h1>...</h1>
<h2>...</h2>
<h3>...</h3>
<h4>...</h4>
<h5>...</h5>
<h6>...</h6>
```

They represent different levels in the document's structure.

For example:

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

The structure can be understood like this:

```text
Web Development
│
├── HTML
│
├── CSS
│
└── JavaScript
```

The `<h1>` represents the main topic.

Each `<h2>` represents a major section within that topic.

---

## 4. Adding Subsections

A heading can contain smaller sections underneath it.

For example:

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

The hierarchy is:

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

The heading levels communicate this hierarchy.

---

## 5. A Heading Should Describe the Content Below It

A heading should give the reader an idea of what the following content is about.

Good:

```html
<h2>HTML Tables</h2>

<p>
    HTML tables allow us to organize information into rows and columns.
</p>
```

The heading clearly describes the paragraph.

Another example:

```html
<h2>Creating Links</h2>

<p>
    The anchor element is used to create hyperlinks between webpages.
</p>
```

The reader immediately knows what the section is about.

---

## 6. Don't Use Headings Just to Make Text Bigger

A common beginner mistake is using a heading because they want large text.

For example:

```html
<h2>Welcome to my website</h2>
```

If "Welcome to my website" is simply normal text that needs to be large, a heading may not be appropriate.

HTML headings should represent **document structure**, not font size.

If you want to make ordinary text larger, CSS should control its appearance:

```html
<p class="large-text">Welcome to my website</p>
```

```css
.large-text {
    font-size: 2rem;
}
```

---

## 7. Don't Skip Heading Levels Just for Appearance

Consider:

```html
<h1>Web Development</h1>

<h3>HTML</h3>
```

This skips `<h2>`.

Generally, heading levels should follow the logical structure of the document.

Better:

```html
<h1>Web Development</h1>

<h2>HTML</h2>
```

And if HTML has smaller topics:

```html
<h1>Web Development</h1>

<h2>HTML</h2>

<h3>Elements</h3>

<h3>Attributes</h3>

<h3>Forms</h3>
```

The important thing is **logical hierarchy**, not simply making every heading smaller than the previous one.

---

## 8. One `<h1>` for the Main Topic

A simple webpage can have a structure such as:

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

Think of `<h1>` as the title of the overall document or main topic.

The `<h2>` elements divide that topic into major sections.

---

## 9. Headings and Paragraphs Create a Document

You can use this pattern throughout a webpage:

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

This makes the webpage easier to read and understand.

It also gives browsers, search engines, screen readers, and other tools a better understanding of how the content is organized.

---

## 10. A Real-World Example

Imagine creating a webpage about Uganda.

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

The structure is:

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

The HTML is therefore not just displaying text. It is describing the **relationship between different pieces of information**.

---

## Quick Rule

When writing content, think:

**Heading → What is this section about?**

**Paragraph → What do I want to say about it?**

For example:

```html
<h2>HTML Forms</h2>

<p>
    HTML forms allow users to enter and submit information to a website.
</p>
```

The heading names the subject, and the paragraph explains it.
