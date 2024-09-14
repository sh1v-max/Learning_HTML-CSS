# CSS Grid

CSS Grid is a powerful layout system that allows you to create two-dimensional grids for structuring content. It is a combination of rows and columns that can be used to create complex layouts.

## Grid Container Properties

The following properties can be used to style the grid container:

* `display: grid;` - This property must be declared in order to create a grid container.
* `grid-template-columns: repeat(3, 1fr);` - This property specifies the width of each column in the grid. The value `repeat(3, 1fr)` creates a grid with three columns, each taking up an equal amount of space.
* `grid-template-rows: 100px 200px;` - This property specifies the height of each row in the grid. The value `100px 200px` creates a grid with two rows, the first row being 100px tall and the second row being 200px tall.
* `grid-column-gap: 10px;` - This property specifies the gap between each column in the grid.
* `grid-row-gap: 15px;` - This property specifies the gap between each row in the grid.
* `justify-items: center;` - This property specifies how the grid items should be justified in their respective cells.
* `align-items: center;` - This property specifies how the grid items should be aligned in their respective cells.

## Grid Item Properties

The following properties can be used to style the grid items:

* `grid-column-start: 2;` - This property specifies the starting column of the grid item.
* `grid-column-end: 4;` - This property specifies the ending column of the grid item.
* `grid-row-start: 1;` - This property specifies the starting row of the grid item.
* `grid-row-end: 3;` - This property specifies the ending row of the grid item.
* `grid-area: header;` - This property specifies the name of the grid area that the item should be placed in.

## Grid Area Properties

The following properties can be used to define a grid area:

* `grid-area: header;` - This property specifies the name of the grid area.
* `grid-template-areas: 'header header header' 'nav main main' 'footer footer footer';` - This property specifies the layout of the grid area.

## Grid Auto Placement

The following properties can be used to control the auto placement of grid items:

* `grid-auto-flow: row;` - This property specifies the direction of the auto placement.
* `grid-auto-flow: column;` - This property specifies the direction of the auto placement.

## Grid Auto Placement Algorithm

The following properties can be used to control the auto placement algorithm of grid items:

* `grid-auto-flow: dense;` - This property specifies that the auto placement algorithm should try to fill in holes in the grid.
* `grid-auto-flow: sparse;` - This property specifies that the auto placement algorithm should not try to fill in holes in the grid.

## Grid Item Placement

The following properties can be used to control the placement of grid items:

* `grid-column: 1 / 3;` - This property specifies the starting and ending columns of the grid item.
* `grid-row: 1 / 3;` - This property specifies the starting and ending rows of the grid item.
* `grid-area: header;` - This property specifies the name of the grid area that the item should be placed in.

## Grid Item Sizing

The following properties can be used to control the sizing of grid items:

* `grid-column: 1 / span 2;` - This property specifies the starting column and the number of columns that the grid item should span.
* `grid-row: 1 / span 2;` - This property specifies the starting row and the number of rows that the grid item should span.

## Grid Item Alignment

The following properties can be used to control the alignment of grid items:

* `justify-self: start;` - This property specifies how the grid item should be justified in its respective cell.
* `justify-self: center;` - This property specifies how the grid item should be justified in its respective cell.
* `justify-self: end;` - This property specifies how the grid item should be justified in its respective cell.
* `align-self: start;` - This property specifies how the grid item should be aligned in its respective cell.
* `align-self: center;` - This property specifies how the grid item should be aligned in its respective cell.
* `align-self: end;` - This property specifies how the grid item should be aligned in its respective cell.


For more information about CSS Overflow, visit: 
> - [W3Schools](https://www.w3schools.com/CSS/css_grid.asp)
> - [YouTube (grid-area)](https://www.youtube.com/watch?v=YulUVlGw7cw&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=40)
