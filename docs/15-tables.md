# 15 - Tables

**Goal:** present true tabular data with `table`,rows, headers, and captions.

> Tables are for **data** (prices, schedules). Never use them for page layout,that era ended.

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
| `caption` | Table title,first child, announced by readers |
| `thead` / `tbody` (`tfoot`) | Header/body(/footer) row groups |
| `tr` | Table row,holds `th`/`td` only |
| `th` | Header cell,bold + centered by default |
| `td` | Data cell |

`scope` tells readers which cells a header labels:

```html
<th scope="col">Price</th>   <!-- labels the column below -->
<th scope="row">Bread</th>   <!-- labels the row beside it -->
```

Merging cells (use sparingly):

```html
<td colspan="2">Sold out</td>
<td rowspan="2">Open daily</td>
```

## Rules

- Every row should end up with the same effective column count,mismatches render ragged.
- `th` without `scope` still works visually but leaves screen-reader users guessing.
- Styling (borders, striping) belongs to CSS,keep markup structural.

## Recap

| Piece | Rule |
|-------|------|
| `caption` | Always,names the table |
| `thead`/`tbody` | Group header vs data rows |
| `th` + `scope` | Label columns/rows for readers |
| `tr` | Contains only `th`/`td` |

**Next:** [16 - Forms Basics](16-forms-basics.md) · **Prev:** [14 - Lists](14-lists.md)
