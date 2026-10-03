# Tables

When you have information that naturally sits in **rows and columns**, marks, prices, timetables, a table is the right tool. Not for layout, but for data where the row/column relationship matters.

## What counts as tabular data?

Think:

* Student marks
* Product prices and quantities
* Class timetables
* Sales records

For example:

| Name  | Age | Class |
| ----- | --: | ----- |
| John  |  15 | S2    |
| Sarah |  14 | S1    |
| David |  16 | S3    |

HTML gives you a handful of elements to build exactly that.

---

# The Basic Table

`<table>` creates the table:

```html
<table>
</table>
```

Empty, of course. You need **rows** and **cells** inside it:

```html
<table>
    <tr>
        <td>John</td>
        <td>15</td>
        <td>S2</td>
    </tr>

    <tr>
        <td>Sarah</td>
        <td>14</td>
        <td>S1</td>
    </tr>
</table>
```

---

# `<tr>`: Table Row

`<tr>` is a **table row**, one horizontal line:

```html
<tr>
</tr>
```

Two rows, for instance:

```html
<table>
    <tr>
        <td>John</td>
        <td>15</td>
    </tr>

    <tr>
        <td>Sarah</td>
        <td>14</td>
    </tr>
</table>
```

```text
John     15
Sarah    14
```

---

# `<td>`: Table Data Cell

`<td>` is a **data cell**, `td` = table data:

```html
<td>John</td>
```

A row can hold several:

```html
<tr>
    <td>John</td>
    <td>15</td>
    <td>S2</td>
</tr>
```

→ three cells: `| John | 15 | S2 |`

---

# `<th>`: Table Header Cell

`<th>` is a **header cell**, `th` = table header. Use it for row or column headings instead of plain `<td>`:

Instead of:

```html
<tr>
    <td>Name</td>
    <td>Age</td>
    <td>Class</td>
</tr>
```

prefer:

```html
<tr>
    <th>Name</th>
    <th>Age</th>
    <th>Class</th>
</tr>
```

Full example:

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Class</th>
    </tr>

    <tr>
        <td>John</td>
        <td>15</td>
        <td>S2</td>
    </tr>

    <tr>
        <td>Sarah</td>
        <td>14</td>
        <td>S1</td>
    </tr>
</table>
```

That first row now properly labels the columns.

---

# `<caption>`: Table Title

`<caption>` gives the table a **title or description** and belongs right after `<table>`:

```html
<table>
    <caption>Student Information</caption>

    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Class</th>
    </tr>

    <tr>
        <td>John</td>
        <td>15</td>
        <td>S2</td>
    </tr>
</table>
```

Think of it as the table's heading, readers and screen readers thank you for it.

---

# `<thead>`: Header Group

`<thead>` groups the header rows:

```html
<table>

    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Class</th>
        </tr>
    </thead>

</table>
```

Particularly useful when tables get longer or you want to style the header separately.

---

# `<tbody>`: Body Group

`<tbody>` wraps the main data rows:

```html
<table>

    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Class</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>John</td>
            <td>15</td>
            <td>S2</td>
        </tr>

        <tr>
            <td>Sarah</td>
            <td>14</td>
            <td>S1</td>
        </tr>
    </tbody>

</table>
```

---

# `<tfoot>`: Footer / Summary

`<tfoot>` groups summary or footer rows, e.g. a total:

```html
<table>

    <thead>
        <tr>
            <th>Product</th>
            <th>Price</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Bread</td>
            <td>5,000</td>
        </tr>

        <tr>
            <td>Milk</td>
            <td>3,000</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <th>Total</th>
            <th>8,000</th>
        </tr>
    </tfoot>

</table>
```

---

# Complete Table Structure

Putting it together, a well-structured table often looks like:

```text
<table>
    <caption>

    <thead>
        <tr>
            <th>
            <th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>
            <td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>
            <td>
        </tr>
    </tfoot>

</table>
```

Concrete example:

```html
<table>

    <caption>Student Marks</caption>

    <thead>
        <tr>
            <th>Name</th>
            <th>Mathematics</th>
            <th>English</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>John</td>
            <td>85</td>
            <td>78</td>
        </tr>

        <tr>
            <td>Sarah</td>
            <td>92</td>
            <td>88</td>
        </tr>
    </tbody>

</table>
```

---

# Rows vs Columns: A Quick Visual

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Class</th>
    </tr>

    <tr>
        <td>John</td>
        <td>15</td>
        <td>S2</td>
    </tr>
</table>
```

→ **2 rows**, **3 columns**:

```text
             Columns
          ↓       ↓       ↓

       | Name | Age | Class |
       |------|-----|-------|
Rows → | John | 15  | S2    |
```

Remember: `<tr>` makes a row; `<th>`/`<td>` make cells *inside* that row.

---

# Spanning Cells

Sometimes a cell should stretch over several rows or columns.

## `colspan`: span columns

```html
<table>
    <tr>
        <th colspan="2">Student Information</th>
    </tr>

    <tr>
        <td>John</td>
        <td>S2</td>
    </tr>
</table>
```

That header now covers two columns.

---

## `rowspan`: span rows

```html
<table>
    <tr>
        <th rowspan="2">Name</th>
        <td>John</td>
    </tr>

    <tr>
        <td>Sarah</td>
    </tr>
</table>
```

"Name" stretches over two rows.

---

# Tables Are for Data, Not Layout

Good fits:

```text
Student | Class | Mark
Product | Price | Quantity
Date    | Event | Location
```

If you're reaching for a table just to position things on the page, pause, layout is a job for CSS (and landmarks like `header`/`main`), not tables.

---

# At a glance

| Element / Attribute | What it does |
| ------------------- | ------------ |
| `<table>` | Creates a table |
| `<caption>` | Title / description for the table |
| `<tr>` | Table row |
| `<th>` | Header cell |
| `<td>` | Data cell |
| `<thead>` | Groups header rows |
| `<tbody>` | Groups main rows |
| `<tfoot>` | Groups footer / summary rows |
| `colspan` | Span multiple columns |
| `rowspan` | Span multiple rows |

---

# Recap

Minimal table:

```html
<table>
    <tr>
        <th>Heading</th>
        <th>Heading</th>
    </tr>

    <tr>
        <td>Data</td>
        <td>Data</td>
    </tr>
</table>
```

More structured:

```html
<table>

    <caption>Table Title</caption>

    <thead>
        <tr>
            <th>Heading</th>
            <th>Heading</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Data</td>
            <td>Data</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>Summary</td>
            <td>Total</td>
        </tr>
    </tfoot>

</table>
```

Keep this in mind:

**`<table>` → `<tr>` → `<th>` / `<td>`**

A table holds rows; each row holds cells.
