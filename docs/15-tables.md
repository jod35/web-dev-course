# 15 - Tables

**Goal:** In this chapter you will learn how to present true tabular data with `table`, rows, headers, and captions.

> Tables are for **data** such as prices and schedules. Never use them for page layout, because that era has ended.

## Minimal table

```html
<table>
  <caption>Morning prices</caption>
  <thead>
    <tr>
      <th scope="col">Item</th>
      <th scope="col">Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bread</td>
      <td>$1</td>
    </tr>
    <tr>
      <td>Milk</td>
      <td>$2</td>
    </tr>
  </tbody>
</table>
```

## Tag reference

| Tag | Job |
|-----|-----|
| `table` | The whole table |
| `caption` | The table title, which is the first child and is announced by readers |
| `thead` / `tbody` (`tfoot`) | Header, body, and footer row groups |
| `tr` | Table row, which holds `th` and `td` only |
| `th` | Header cell, which is bold and centred by default |
| `td` | Data cell |

The `scope` attribute tells readers which cells a header labels:

```html
<th scope="col">Price</th>   <!-- labels the column below -->
<th scope="row">Bread</th>   <!-- labels the row beside it -->
```

Cells can be merged, although this technique should be used sparingly:

```html
<td colspan="2">Sold out</td>
<td rowspan="2">Open daily</td>
```

## Rules

- Every row should end up with the same effective column count, because mismatches render as ragged tables.
- A `th` element without a `scope` attribute still works visually, but it leaves screen-reader users guessing about the relationship.
- Styling such as borders and striping belongs to CSS, so keep the markup structural.

## Recap

| Piece | Rule |
|-------|------|
| `caption` | Always include it in order to name the table |
| `thead`/`tbody` | Group header rows separately from data rows |
| `th` plus `scope` | Label columns and rows for readers |
| `tr` | Contains only `th` and `td` |

**Next:** [16 - Forms Basics](16-forms-basics.md) · **Prev:** [14 - Lists](14-lists.md)
