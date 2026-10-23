# Build Your First Page

This chapter puts the previous lessons together. You will build a complete page with a title, sections, paragraphs, and a thematic break. The content is a school notice, but you can replace it with anything you know well.

## 1. Create the file

Create a folder for the exercise. Inside it, create a file called `index.html`.

Start with the page skeleton:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>School Notice</title>
</head>
<body>

</body>
</html>
```

The `<title>` appears in the browser tab. The visible content goes inside `<body>`.

## 2. Add the main heading

```html
<body>
  <h1>Sports Day</h1>
  <p>Sports Day will take place on Friday, 6 November.</p>
</body>
```

There is one `<h1>` because the page has one main topic.

## 3. Add sections

Use `<h2>` for the main parts of the notice:

```html
<body>
  <h1>Sports Day</h1>
  <p>Sports Day will take place on Friday, 6 November.</p>

  <h2>Time and place</h2>
  <p>The event starts at 8am on the school field. Students should arrive by 7:30am.</p>

  <h2>What to bring</h2>
  <p>Bring a water bottle, a hat, and sports shoes. Lunch will be provided.</p>

  <h2>Parents and guardians</h2>
  <p>Parents are welcome to attend. Seating will be available near the finish line.</p>
</body>
```

Each `<h2>` introduces one section. Each paragraph gives the detail for that section.

## 4. Add a closing note

Use `<hr>` to separate the main notice from an unrelated note:

```html
  <h2>Parents and guardians</h2>
  <p>Parents are welcome to attend. Seating will be available near the finish line.</p>

  <hr>

  <p>If it rains, the event will move to the school hall.</p>
```

Do not use several `<br>` elements to create the same gap.

## 5. Check the page

Open `index.html` in your browser. Check:

- The browser tab shows "School Notice".
- There is one main heading.
- Every section has a heading and at least one paragraph.
- The line under the closing note separates it from the main notice.
- The page is readable when you make the browser window narrow.

## 6. Improve the content

Rewrite the notice for something you know: a football match, a school trip, a club meeting, or a shop opening. Keep the same structure:

1. One `<h1>`.
2. Two or three `<h2>` sections.
3. One paragraph per idea.
4. One `<hr>` only if you need a real break in topic.

## What you have practised

- Nesting elements inside `<body>`.
- Choosing heading levels by structure, not size.
- Writing paragraphs around one idea.
- Using `<hr>` for a change of topic.
- Checking a page in the browser instead of assuming it works.

Next: [Emphasis and Meaning](07-meaning-vs-looks.md)
