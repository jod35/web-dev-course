# Tables

**Goal:** In this chapter, you will learn how to use HTML tables to organize related information into **rows and columns**. You will learn how to create tables, add headings and data, group rows, and add captions.

## What is an HTML Table?

An HTML table is used to present information in **rows and columns**.

Tables are useful for information such as:

* Student marks
* Product prices
* Class timetables
* Employee information
* Sales records
* Schedules

For example:

| Name  | Age | Class |
| ----- | --: | ----- |
| John  |  15 | S2    |
| Sarah |  14 | S1    |
| David |  16 | S3    |

In HTML, this information can be represented using several elements.

---

# The Basic Table

The `<table>` element creates a table.

```html
<table>
</table>
```

However, an empty table does not contain any information. We need to add **rows** and **cells**.

A simple table looks like this:

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

# `<tr>` - Table Row

The `<tr>` element creates a **table row**.

```html
<tr>
</tr>
```

Each `<tr>` represents one horizontal row in the table.

For example:

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

This creates two rows.

```text
John     15
Sarah    14
```

---

# `<td>` - Table Data Cell

The `<td>` element represents a **cell containing table data**.

`td` means **table data**.

```html
<td>John</td>
```

A row can contain multiple data cells:

```html
<tr>
    <td>John</td>
    <td>15</td>
    <td>S2</td>
</tr>
```

This row has three cells.

```text
| John | 15 | S2 |
```

---

# `<th>` - Table Header Cell

The `<th>` element represents a **heading for a row or column**.

`th` means **table header**.

Instead of:

```html
<tr>
    <td>Name</td>
    <td>Age</td>
    <td>Class</td>
</tr>
```

use:

```html
<tr>
    <th>Name</th>
    <th>Age</th>
    <th>Class</th>
</tr>
```

A complete table might look like:

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

The first row contains the column headings.

---

# `<caption>` - Table Caption

The `<caption>` element gives a table a **title or description**.

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

The caption describes what the table is about.

A `<caption>` should be placed immediately after the opening `<table>` tag.

---

# `<thead>` - Table Header

The `<thead>` element groups the rows containing the table's header information.

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

It is particularly useful for larger or more structured tables.

---

# `<tbody>` - Table Body

The `<tbody>` element groups the main data rows of a table.

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

The `<tbody>` contains the main information in the table.

---

# `<tfoot>` - Table Footer

The `<tfoot>` element groups rows containing summary or footer information.

For example, a sales table might contain a total:

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

A well-structured table can contain:

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

A complete example:

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

# Understanding Rows and Columns

Consider this table:

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

The table has **2 rows** and **3 columns**.

```text
             Columns
          ↓       ↓       ↓

       | Name | Age | Class |
       |------|-----|-------|
Rows → | John | 15  | S2    |
```

A `<tr>` creates a row.

A `<th>` or `<td>` creates a cell within that row.

---

# Combining Cells

HTML allows cells to span multiple rows or columns.

## `colspan`

The `colspan` attribute allows a cell to span multiple **columns**.

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

The header cell spans two columns.

---

## `rowspan`

The `rowspan` attribute allows a cell to span multiple **rows**.

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

The `Name` cell spans two rows.

---

# Tables Are for Tabular Data

Tables should be used when information has a meaningful relationship between **rows and columns**.

Good examples include:

```text
Student | Class | Mark
Product | Price | Quantity
Date    | Event | Location
```

Tables should not be used simply to position elements on a webpage. Page layout should be handled using modern HTML and CSS.

---

# Important Elements and Attributes

| Element/Attribute | Purpose                                |
| ----------------- | -------------------------------------- |
| `<table>`         | Creates a table                        |
| `<caption>`       | Gives the table a title or description |
| `<tr>`            | Creates a table row                    |
| `<th>`            | Creates a header cell                  |
| `<td>`            | Creates a data cell                    |
| `<thead>`         | Groups table header rows               |
| `<tbody>`         | Groups the main table rows             |
| `<tfoot>`         | Groups footer or summary rows          |
| `colspan`         | Makes a cell span multiple columns     |
| `rowspan`         | Makes a cell span multiple rows        |

---

# Recap

The basic table structure is:

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

For a more structured table:

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

The key idea is:

**`<table>` → `<tr>` → `<th>` / `<td>`**

A table contains rows, and each row contains cells.
