# HTML Tables

## Table of Contents

1. [Introduction to HTML Tables](#introduction-to-html-tables)  
2. [Basic Table Structure](#basic-table-structure)  
3. [Table Rows and Columns](#table-rows-and-columns)  
4. [Table Headers](#table-headers)  
5. [Table Attributes](#table-attributes)  
6. [Merging Cells (Rowspan and Colspan)](#merging-cells-rowspan-and-colspan)  
7. [Styling Tables](#styling-tables)  
8. [Conclusion](#conclusion)  


## Introduction to HTML Tables

HTML tables are used to organize and display data in a tabular format, which consists of rows and columns. Tables are created using the `<table>` tag, and data is organized using rows (`<tr>`) and cells (`<td>` or `<th>`).


## Basic Table Structure

A simple table includes the following elements:
- `<table>`: Defines the table.
- `<tr>`: Defines a row in the table.
- `<td>`: Defines a cell (data) in a row.

### Example:

```html
<h3>Basic Table Example</h3>
<table border="1">
  <tr>
    <td>Row 1, Cell 1</td>
    <td>Row 1, Cell 2</td>
  </tr>
  <tr>
    <td>Row 2, Cell 1</td>
    <td>Row 2, Cell 2</td>
  </tr>
</table>
```


## Table Rows and Columns

- **Rows** are defined using `<tr>` (table row).  
- **Columns** (data) are defined using `<td>` (table data cell).

### Example with Rows and Columns:

```html
<h3>Table with Rows and Columns</h3>
<table border="1">
  <tr>
    <td>Cell 1</td>
    <td>Cell 2</td>
    <td>Cell 3</td>
  </tr>
  <tr>
    <td>Cell 4</td>
    <td>Cell 5</td>
    <td>Cell 6</td>
  </tr>
</table>
```


## Table Headers

Table headers are defined using the `<th>` tag. Headers are typically bold and centered.

### Example with Table Headers:

```html
<h3>Table with Headers</h3>
<table border="1">
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>City</th>
  </tr>
  <tr>
    <td>John</td>
    <td>25</td>
    <td>New York</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>30</td>
    <td>Chicago</td>
  </tr>
</table>
```


## Table Attributes

HTML tables support several attributes to control their behavior.

- **`border`**: Specifies the border size for the table.  
- **`cellpadding`**: Adds space between the cell content and cell border.  
- **`cellspacing`**: Adds space between table cells.  
- **`width` and `height`**: Sets the table or cell dimensions.

### Example with Attributes:

```html
<h3>Table with Attributes</h3>
<table border="2" cellpadding="10" cellspacing="5" width="50%">
  <tr>
    <th>Product</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>Laptop</td>
    <td>$800</td>
  </tr>
  <tr>
    <td>Phone</td>
    <td>$500</td>
  </tr>
</table>
```

## Merging Cells (Rowspan and Colspan)

- **`rowspan`**: Merges cells vertically across rows.  
- **`colspan`**: Merges cells horizontally across columns.

### Example with Rowspan and Colspan:

```html
<h3>Table with Merged Cells</h3>
<table border="1">
  <tr>
    <th rowspan="2">Name</th>
    <th colspan="2">Contact</th>
  </tr>
  <tr>
    <td>Email</td>
    <td>Phone</td>
  </tr>
  <tr>
    <td>John</td>
    <td>john@example.com</td>
    <td>123-456-7890</td>
  </tr>
</table>
```


## Styling Tables

HTML tables can be styled using CSS to improve their appearance.

### Example with CSS Styling:

```html
<h3>Styled Table Example</h3>
<style>
  table {
    width: 60%;
    border-collapse: collapse;
  }
  th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: center;
  }
  th {
    background-color: #f2f2f2;
  }
</style>

<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>28</td>
    <td>Canada</td>
  </tr>
  <tr>
    <td>Bob</td>
    <td>35</td>
    <td>USA</td>
  </tr>
</table>
```

## Conclusion

HTML tables are a powerful way to organize and display data. By using rows, columns, headers, and attributes like `rowspan` and `colspan`, developers can create structured and visually appealing tables.
