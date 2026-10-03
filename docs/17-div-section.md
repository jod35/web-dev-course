# Grouping: div, section, span

As pages get bigger, you'll need ways to bundle related bits together. `<div>`, `<section>` and `<span>` all group content — but they signal different things.

## Why group at all?

Imagine a page outline:

```text
Header
    Navigation

Main content
    About us
    Our services

Footer
```

Without grouping, everything's just floating. HTML gives you distinct elements for those bundles.

---

# `<div>` — Generic Block Container

`<div>` is your **generic block wrapper** — it groups content without saying what it means:

```html
<div>
    <h2>About Us</h2>
    <p>We build software for businesses.</p>
</div>
```

It simply says:

> These elements belong together.

That's why `<div>` is handy when no more specific semantic element fits.

---

## `<div>` as a Container

A `<div>` can hold pretty much anything:

```html
<div>
    <h2>Student Information</h2>

    <p>Name: Jonathan</p>
    <p>Class: S2</p>

    <a href="profile.html">View Profile</a>
</div>
```

It keeps that cluster together and gives CSS or JavaScript a convenient hook to target.

---

# `<section>` — A Thematic Section

`<section>` is for a **thematically related chunk** of the document — a section with its own topic:

```html
<section>
    <h2>About Us</h2>

    <p>
        We teach students how to build websites.
    </p>
</section>
```

Unlike `<div>`, it carries meaning:

> This is a distinct section of the document.

---

## Sections Usually Have a Heading

A heading that labels the section helps readers and assistive tech:

```html
<section>
    <h2>Our Services</h2>

    <p>We provide web development services.</p>
</section>
```

Followed by another:

```html
<section>
    <h2>Contact Us</h2>

    <p>Get in touch with our team.</p>
</section>
```

Those headings are part of the structure, not just decoration.

---

# `<div>` vs `<section>` — Which One?

```html
<div>
    <h2>About Us</h2>
    <p>We teach programming.</p>
</div>
```

vs.

```html
<section>
    <h2>About Us</h2>
    <p>We teach programming.</p>
</section>
```

Both will group, but they say different things:

* **`<div>`** → "Grouped together." No semantics attached.
* **`<section>`** → "This is a meaningful section."

If the bundle represents a real topic-based section, prefer `<section>`. If you just need a generic box for styling or scripting and nothing semantic fits, use `<div>`.

---

# `<span>` — Generic Inline Container

`<span>` is the inline cousin — it wraps **small pieces inside a line**:

```html
<p>
    My favourite language is
    <span>Python</span>.
</p>
```

Unlike `<div>`, it doesn't start a new block — it stays in the flow of text.

```html
<p>Hello <span>Jonathan</span>, welcome!</p>
```

That `<span>` is part of the same paragraph, not a separate block.

---

# `<span>` for Part of a Sentence

You'll often want to flag a particular phrase:

```html
<p>
    The weather today is
    <span>very warm</span>.
</p>
```

By itself `<span>` doesn't add meaning — it just identifies that slice so you can style or script it.

---

# `<span>` vs `<div>` — Inline vs Block

**`<div>`** — block-level:

```html
<div>
    First group
</div>

<div>
    Second group
</div>
```
→ each group sits on its own line/ block.

**`<span>`** — inline:

```html
<p>
    This is <span>one</span> sentence.
</p>
```
→ stays within the surrounding line.

Think: **block vs inline** is the core split.

---

# Grouping with Classes and IDs

These grouping elements get most useful with `class` or `id`:

```html
<div class="card">
    <h2>Python</h2>
    <p>A programming language.</p>
</div>
```

A class marks a category — several elements can share it:

```html
<section class="course">
    <h2>Python Course</h2>
</section>

<section class="course">
    <h2>HTML Course</h2>
</section>
```

An `id` identifies one unique element:

```html
<div id="main-content">
    <h1>Welcome</h1>
</div>
```

You'll lean on them heavily once you add CSS and JavaScript.

---

# Bringing Them Together

A page can use all three at once:

```html
<section>

    <h2>Our Courses</h2>

    <div class="course">
        <h3>HTML</h3>
        <p>Learn how to build <span>web pages</span>.</p>
    </div>

    <div class="course">
        <h3>Python</h3>
        <p>Learn how to build <span>programs</span>.</p>
    </div>

</section>
```

* `<section>` → the **Courses section** as a whole.
* `<div>` → each individual course card.
* `<span>` → a small inline highlight inside the paragraph.

---

# How to Choose

Ask what the grouping *means*:

* **A distinct thematic section?** → `<section>`:
```html
<section>
    <h2>Our Services</h2>
    ...
</section>
```

* **Just need a generic block box?** → `<div>`:
```html
<div>
    ...
</div>
```

* **A small inline slice?** → `<span>`:
```html
<p>This is <span>important</span> information.</p>
```

---

# At a glance

| Element | What it's for |
| ------- | ------------- |
| `<section>` | Groups thematically related content |
| `<div>` | Generic block-level container |
| `<span>` | Generic inline container |
| `class` | Marks elements as belonging to a group |
| `id` | Unique identifier for one element |

---

# Recap

In short:

```text
<section>
    A meaningful section of the document
</section>

<div>
    A generic block-level group
</div>

<p>
    Some text with a
    <span>small inline group</span>
    inside it.
</p>
```

Mental shorthand:

**`<section>` = meaningful group**

**`<div>` = generic block**

**`<span>` = generic inline**
