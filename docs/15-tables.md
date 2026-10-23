# Tables

Tables are for data that belongs in rows and columns: marks, prices, timetables, and records. They are not for page layout. CSS handles layout now.

## The basic structure

A table contains rows, and each row contains cells:

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

- `<table>` creates the table.
- `<tr>` creates a row.
- `<td>` creates a data cell.

The example above is hard to read because the first row is data, not headings. Tables usually need header cells.

## Header cells: `<th>`

Use `<th>` for header cells. Add `scope="col"` for column headings and `scope="row"` for row headings:

```html
<table>
  <tr>
    <th scope="col">Name</th>
    <th scope="col">Age</th>
    <th scope="col">Class</th>
  </tr>
  <tr>
    <td>John</td>
    <td>15</td>
    <td>S2</td>
  </tr>
</table>
```

`scope` tells assistive technology which cells a heading applies to. It is especially important in larger tables.

## A caption

Give the table a title with `<caption>`:

```html
<table>
  <caption>Student Information</caption>
  <tr>
    <th scope="col">Name</th>
    <th scope="col">Age</th>
    <th scope="col">Class</th>
  </tr>
  <tr>
    <td>John</td>
    <td>15</td>
    <td>S2</td>
  </tr>
</table>
```

The caption goes immediately after `<table>`. It helps everyone understand what the table contains.

## Grouping rows

Longer tables can be grouped into a head, body, and foot:

```html
<table>
  <caption>Bakery Prices</caption>

  <thead>
    <tr>
      <th scope="col">Item</th>
      <th scope="col">Price</th>
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
      <th scope="row">Total</th>
      <td>8,000</td>
    </tr>
  </tfoot>
</table>
```

- `<thead>` groups the header rows.
- `<tbody>` groups the main data rows.
- `<tfoot>` groups summary or footer rows.

Grouping is useful for styling and for very long tables. A small table does not always need all three.

## Spanning cells

Use `colspan` when a cell should cover more than one column:

```html
<tr>
  <th scope="colgroup" colspan="2">Student Information</th>
</tr>
<tr>
  <td>John</td>
  <td>S2</td>
</tr>
```

Use `rowspan` when a cell should cover more than one row:

```html
<tr>
  <th scope="rowgroup" rowspan="2">Name</th>
  <td>John</td>
</tr>
<tr>
  <td>Sarah</td>
</tr>
```

Spanning makes a table harder to read and harder to maintain. Use it only when the data really has that shape.

## A complete timetable

```html
<table>
  <caption>Term Two Timetable</caption>

  <thead>
    <tr>
      <th scope="col">Time</th>
      <th scope="col">Monday</th>
      <th scope="col">Tuesday</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <th scope="row">8:00</th>
      <td>Mathematics</td>
      <td>English</td>
    </tr>
    <tr>
      <th scope="row">9:00</th>
      <td>Biology</td>
      <td>Chemistry</td>
    </tr>
    <tr>
      <th scope="row">10:00</th>
      <td colspan="2">Break</td>
    </tr>
  </tbody>
</table>
```

The row headings make it clear which time each row describes. The break spans both days.

## Check your work

- Is the table used for data, not layout?
- Does it have a caption?
- Are column headings `<th scope="col">` and row headings `<th scope="row">`?
- Does every row have the right number of cells?
- Does the table still make sense when read aloud row by row?

## Try it

Build a table for a class timetable or a price list. Include:

1. a caption,
2. column headings with `scope="col"`,
3. at least three rows of data,
4. one row heading with `scope="row"`,
5. one cell that spans two columns, only if the data needs it.

Open the page and check that the columns line up. Then add a long item name and see whether the table stays readable.

Next: [Forms](16-forms-basics.md)
