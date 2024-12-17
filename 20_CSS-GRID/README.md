# CSS Grid
## What is CSS Grid?

CSS Grid Layout enables you to create web layouts that can align items into rows and columns. Unlike Flexbox, which is primarily a one-dimensional layout system (either in a row or a column), Grid allows for two-dimensional control (both rows and columns simultaneously).

With CSS Grid, you can:
- Divide the page into rows and columns.
- Position elements within the grid.
- Define flexible and responsive grid layouts.
- Control the alignment and spacing of grid items.


## Basic Syntax of CSS Grid

The main concept of CSS Grid involves defining a **container** and then defining how items should be positioned inside that container. Here's the basic syntax for setting up a grid:

### 1. **Creating a Grid Container**

```css
.container {
  display: grid; /* Declares the container as a grid */
  grid-template-columns: value1 value2 ...; /* Defines the columns */
  grid-template-rows: value1 value2 ...; /* Defines the rows */
}
```

- **`display: grid`**: Makes the element a grid container.
- **`grid-template-columns`**: Defines the size of the columns in the grid.
- **`grid-template-rows`**: Defines the size of the rows in the grid.

### 2. **Grid Items**

Grid items are the child elements inside the grid container. These items will automatically be placed inside the grid by the browser, but you can control their position using grid properties like `grid-column` and `grid-row`.

```css
.item {
  grid-column: span 2; /* Specifies how many columns an item spans */
  grid-row: span 1; /* Specifies how many rows an item spans */
}
```


## Defining Columns and Rows

### 1. **`grid-template-columns`**

The `grid-template-columns` property defines the number of columns and their respective sizes.

- You can specify column sizes using fixed values (e.g., `px`, `em`, `rem`) or relative values (e.g., `%`, `fr`).

#### Example 1: Fixed Number of Columns
```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px; /* 3 fixed-width columns */
}
```

#### Example 2: Flexible Columns
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /* 3 equal-width columns using fractional units */
}
```

#### Example 3: Using `fr` (Fractional Unit)
The `fr` unit is a fractional unit of available space in the grid container.

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr; /* 1st column takes 1/3 of the space, 2nd column takes 2/3 */
}
```

### 2. **`grid-template-rows`**

Similarly to columns, the `grid-template-rows` property defines the number of rows and their respective sizes.

```css
.container {
  display: grid;
  grid-template-rows: 100px 200px 300px; /* 3 fixed-height rows */
}
```


## Grid Item Placement

Once the grid container is defined, you can place items inside the grid using grid lines. By default, grid items are placed into the next available cell, but you can control their exact position.

### 1. **Placing Grid Items with `grid-column` and `grid-row`**

- **`grid-column`**: Specifies the horizontal placement of an item (which column to start and end at).
- **`grid-row`**: Specifies the vertical placement of an item (which row to start and end at).

#### Example: Positioning an Item
```css
.item1 {
  grid-column: 1 / 3; /* Starts at column 1 and ends at column 3 */
  grid-row: 1 / 2; /* Starts at row 1 and ends at row 2 */
}
```

#### Example: Spanning Multiple Columns or Rows
```css
.item2 {
  grid-column: span 2; /* Spans 2 columns */
  grid-row: span 2; /* Spans 2 rows */
}
```

## Creating a Responsive Grid with `auto` and `fr`

To make your grid layout responsive, you can use the `auto` keyword and the `fr` unit. This allows you to create layouts that adapt to the size of the container.

#### Example: Responsive Layout
```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); /* Creates columns that automatically adjust */
}
```

In this example, `auto-fill` will create as many columns as possible, with each column having a minimum width of 200px and a flexible maximum width that takes up the remaining space.


## Gap Between Grid Items

You can control the space between the grid items (both columns and rows) using the `gap` property (formerly `grid-gap`).

### Syntax:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px; /* Adds 20px gap between both rows and columns */
}
```

### You can also specify different gaps for rows and columns:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 100px;
  column-gap: 20px; /* Adds gap only between columns */
  row-gap: 30px;    /* Adds gap only between rows */
}
```


## Alignment and Justification in CSS Grid

CSS Grid provides several alignment and justification properties that allow you to position items within the grid container.

### 1. **`justify-items`** and **`align-items`**

These properties control the alignment of grid items within their individual grid areas.

- **`justify-items`**: Aligns items along the row (horizontal axis).
- **`align-items`**: Aligns items along the column (vertical axis).

```css
.container {
  display: grid;
  justify-items: center; /* Centers items horizontally */
  align-items: center;   /* Centers items vertically */
}
```

### 2. **`justify-content`** and **`align-content`**

These properties control the alignment of the entire grid container's content.

- **`justify-content`**: Aligns the entire grid along the horizontal axis.
- **`align-content`**: Aligns the entire grid along the vertical axis.

```css
.container {
  display: grid;
  justify-content: space-between; /* Distributes grid items evenly along the row */
  align-content: space-around;    /* Distributes grid items evenly along the column */
}
```


## Example: Simple Grid Layout

Here's a simple example that uses CSS Grid to create a basic 3x3 grid layout:

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 equal-width columns */
  grid-template-rows: repeat(3, 100px);  /* 3 rows, each 100px tall */
  gap: 10px; /* Adds 10px space between items */
}

.item {
  background-color: lightblue;
  border: 1px solid #333;
  padding: 20px;
  text-align: center;
}
```

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
  <div class="item">Item 4</div>
  <div class="item">Item 5</div>
  <div class="item">Item 6</div>
  <div class="item">Item 7</div>
  <div class="item">Item 8</div>
  <div class="item">Item 9</div>
</div>
```

In this example:
- The container is divided into a 3x3 grid with equal columns and rows.
- Each grid item is placed within the grid and given some basic styling.

## Summary
### Grid Container Properties

The following properties can be used to style the grid container:

* `display: grid;` - This property must be declared in order to create a grid container.
* `grid-template-columns: repeat(3, 1fr);` - This property specifies the width of each column in the grid. The value `repeat(3, 1fr)` creates a grid with three columns, each taking up an equal amount of space.
* `grid-template-rows: 100px 200px;` - This property specifies the height of each row in the grid. The value `100px 200px` creates a grid with two rows, the first row being 100px tall and the second row being 200px tall.
* `grid-column-gap: 10px;` - This property specifies the gap between each column in the grid.
* `grid-row-gap: 15px;` - This property specifies the gap between each row in the grid.
* `justify-items: center;` - This property specifies how the grid items should be justified in their respective cells.
* `align-items: center;` - This property specifies how the grid items should be aligned in their respective cells.

### Grid Item Properties

The following properties can be used to style the grid items:

* `grid-column-start: 2;` - This property specifies the starting column of the grid item.
* `grid-column-end: 4;` - This property specifies the ending column of the grid item.
* `grid-row-start: 1;` - This property specifies the starting row of the grid item.
* `grid-row-end: 3;` - This property specifies the ending row of the grid item.
* `grid-area: header;` - This property specifies the name of the grid area that the item should be placed in.

### Grid Area Properties

The following properties can be used to define a grid area:

* `grid-area: header;` - This property specifies the name of the grid area.
* `grid-template-areas: 'header header header' 'nav main main' 'footer footer footer';` - This property specifies the layout of the grid area.

### Grid Auto Placement

The following properties can be used to control the auto placement of grid items:

* `grid-auto-flow: row;` - This property specifies the direction of the auto placement.
* `grid-auto-flow: column;` - This property specifies the direction of the auto placement.

### Grid Auto Placement Algorithm

The following properties can be used to control the auto placement algorithm of grid items:

* `grid-auto-flow: dense;` - This property specifies that the auto placement algorithm should try to fill in holes in the grid.
* `grid-auto-flow: sparse;` - This property specifies that the auto placement algorithm should not try to fill in holes in the grid.

### Grid Item Placement

The following properties can be used to control the placement of grid items:

* `grid-column: 1 / 3;` - This property specifies the starting and ending columns of the grid item.
* `grid-row: 1 / 3;` - This property specifies the starting and ending rows of the grid item.
* `grid-area: header;` - This property specifies the name of the grid area that the item should be placed in.

### Grid Item Sizing

The following properties can be used to control the sizing of grid items:

* `grid-column: 1 / span 2;` - This property specifies the starting column and the number of columns that the grid item should span.
* `grid-row: 1 / span 2;` - This property specifies the starting row and the number of rows that the grid item should span.

### Grid Item Alignment

The following properties can be used to control the alignment of grid items:

* `justify-self: start;` - This property specifies how the grid item should be justified in its respective cell.
* `justify-self: center;` - This property specifies how the grid item should be justified in its respective cell.
* `justify-self: end;` - This property specifies how the grid item should be justified in its respective cell.
* `align-self: start;` - This property specifies how the grid item should be aligned in its respective cell.
* `align-self: center;` - This property specifies how the grid item should be aligned in its respective cell.
* `align-self: end;` - This property specifies how the grid item should be aligned in its respective cell.


## Conclusion

CSS Grid is a powerful and flexible layout tool that allows you to create complex, responsive designs. With its two-dimensional control over rows and columns, it provides much more power and flexibility than other layout systems like `float` or `flexbox` when building intricate grid-based layouts. By mastering CSS Grid, you can create modern, adaptive layouts for your web pages. 

## Reference
For more information about CSS Grid, visit: 
> - [W3Schools](https://www.w3schools.com/CSS/css_grid.asp)
> - [YouTube (part-1)](https://www.youtube.com/watch?v=npLvEXoLVZQ&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=37&pp=iAQB)
> - [YouTube (part-2)](https://www.youtube.com/watch?v=p-CfOVelX3o&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=38&pp=iAQB)
