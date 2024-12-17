# CSS Flexbox

CSS Flexbox (Flexible Box Layout) is a layout model designed to arrange and distribute elements within a container efficiently, even when their sizes are unknown or dynamic. Flexbox makes it easier to create complex layouts and alignments compared to traditional CSS layout methods like floats or inline-block elements.

In this guide, we'll cover the core concepts and properties of Flexbox to help you understand how to use it for building responsive layouts.


## What is Flexbox?

Flexbox is a one-dimensional layout model that allows items (flex items) within a container (flex container) to be arranged and aligned in a flexible way. Flexbox can align items horizontally or vertically, distribute space evenly, and automatically adjust the layout depending on available space.

### Key Terms:
- **Flex Container**: The parent element that holds the flex items. It is defined using `display: flex` or `display: inline-flex`.
- **Flex Items**: The children elements of the flex container, which will be arranged by Flexbox.

## Setting up Flexbox

To use Flexbox, you need to apply the `display: flex` or `display: inline-flex` property to a container. By default, Flexbox arranges its items in a horizontal row.

### Basic Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      display: flex; /* Turns the container into a flex container */
      background-color: lightgray;
      padding: 10px;
    }

    .item {
      background-color: lightcoral;
      margin: 5px;
      padding: 10px;
      flex: 1; /* Flex item will grow to fill available space */
    }
  </style>
  <title>Flexbox Example</title>
</head>
<body>
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
  </div>
</body>
</html>
```

In the above example:
- `.container` is the flex container with `display: flex`.
- `.item` elements are flex items inside the container.


## Flex Container Properties

These properties apply to the **flex container** and control the layout and behavior of the flex items.

### 1. `display: flex` | `display: inline-flex`
- **`flex`**: Makes the container a block-level flex container.
- **`inline-flex`**: Makes the container an inline flex container (acts like an inline element).

```css
.container {
  display: flex; /* Block-level flex container */
  /* Or */
  display: inline-flex; /* Inline flex container */
}
```

### 2. `flex-direction`
- Specifies the direction in which flex items are placed in the flex container. It can be one of the following:
  - `row`: Default. Items are placed horizontally (left to right).
  - `row-reverse`: Items are placed horizontally (right to left).
  - `column`: Items are placed vertically (top to bottom).
  - `column-reverse`: Items are placed vertically (bottom to top).

```css
.container {
  display: flex;
  flex-direction: row; /* Horizontal layout */
  /* Or */
  flex-direction: column; /* Vertical layout */
}
```

### 3. `flex-wrap`
- Controls whether the flex items should wrap onto the next line if they don't fit in the container. It can be:
  - `nowrap`: Default. Flex items will not wrap and will overflow.
  - `wrap`: Flex items will wrap to the next line if needed.
  - `wrap-reverse`: Flex items will wrap to the previous line (upward for rows).

```css
.container {
  display: flex;
  flex-wrap: wrap; /* Allow items to wrap */
}
```

### 4. `justify-content`
- Aligns flex items along the main axis (horizontally for `row` direction, vertically for `column` direction). Possible values:
  - `flex-start`: Align items to the start (default).
  - `flex-end`: Align items to the end.
  - `center`: Align items to the center.
  - `space-between`: Distribute items with equal space between them.
  - `space-around`: Distribute items with equal space around them.
  - `space-evenly`: Distribute items with equal space between and around them.

```css
.container {
  display: flex;
  justify-content: center; /* Center items horizontally */
}
```

### 5. `align-items`
- Aligns flex items along the cross axis (perpendicular to the main axis). Possible values:
  - `stretch`: Stretch items to fill the container (default).
  - `flex-start`: Align items to the start of the container.
  - `flex-end`: Align items to the end of the container.
  - `center`: Align items to the center of the container.
  - `baseline`: Align items to their baseline.

```css
.container {
  display: flex;
  align-items: center; /* Vertically center items */
}
```

### 6. `align-content`
- Aligns flex lines when there is more than one line of items. This property is similar to `align-items`, but it affects multiple lines instead of individual items. Possible values:
  - `stretch`: Stretch lines to fill the container (default).
  - `flex-start`: Align lines to the start of the container.
  - `flex-end`: Align lines to the end of the container.
  - `center`: Align lines to the center of the container.
  - `space-between`: Distribute lines with equal space between them.
  - `space-around`: Distribute lines with equal space around them.
  - `space-evenly`: Distribute lines with equal space between and around them.

```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: center; /* Align multiple lines of items to the center */
}
```


## Flex Item Properties

These properties apply to the **flex items** (the children of the flex container).

### 1. `flex-grow`
- Defines the ability of a flex item to grow relative to other items if there is extra space in the container. Default is `0` (no growth).
  
```css
.item {
  flex-grow: 1; /* Item will grow to fill available space */
}
```

### 2. `flex-shrink`
- Defines the ability of a flex item to shrink if the container is too small. Default is `1` (items can shrink).
  
```css
.item {
  flex-shrink: 1; /* Item can shrink */
}
```

### 3. `flex-basis`
- Specifies the initial size of a flex item before any growing or shrinking. Can be set to a specific length (e.g., `px`, `em`, `%`), or `auto` (use the item’s natural size).

```css
.item {
  flex-basis: 200px; /* Initial size of the item */
}
```

### 4. `flex`
- A shorthand property for setting `flex-grow`, `flex-shrink`, and `flex-basis` together. The syntax is:
  ```css
  flex: flex-grow flex-shrink flex-basis;
  ```

Example:
```css
.item {
  flex: 1 1 200px; /* Grow, shrink, and set initial size */
}
```

### 5. `align-self`
- Overrides the `align-items` property for a specific flex item. It can be one of the same values as `align-items`.
  
```css
.item {
  align-self: flex-end; /* Align this specific item to the end */
}
```



## Example: Flexbox Layout with Multiple Properties

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      display: flex;
      flex-wrap: wrap; /* Allow wrapping */
      justify-content: space-between; /* Distribute items evenly */
      align-items: center; /* Vertically center items */
      height: 100vh; /* Full viewport height */
    }

    .item {
      background-color: lightcoral;
      padding: 20px;
      flex: 1 1 200px; /* Allow items to grow and shrink */
      margin: 10px;
      text-align: center;
    }
  </style>
  <title>Flexbox Layout</title>
</head>
<body>
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
    <div class="item">Item 4</div>
  </div>
</body>
</html>
```
## Summary 
The main properties and values used in flexbox are:

- `display: flex;` : The container element which contains the flex items.
- `flex-direction: row | column | row-reverse | column-reverse;` : To define the direction of the flex items. Row is the default direction.
- `justify-content: flex-start | center | space-between | space-around;` : To define how the flex items are positioned in the container.
- `flex-wrap: wrap | nowrap;` : To define whether the flex items should wrap to a new line or not.
- `align-items: flex-start | center | stretch;` : To define how the flex items are aligned vertically.
- `align-self: auto | flex-start | center | stretch;` : To define the alignment for an individual flex item.
- `flex-grow: 0 | 1;` : To define how much a flex item should grow relative to the other flex items.
- `flex-shrink: 0 | 1;` : To define how much a flex item should shrink relative to the other flex items.
- `flex-basis: auto | 0 | 100px;` : To define the initial length of a flex item.
- `order: 0 | 1 | 2;` : To define the order of the flex items.

The most common use of flexbox is for creating horizontal or vertical navigation bars, creating responsive image galleries, and creating flexible grid systems.

### Example

The following example demonstrates how to use flexbox to create a horizontal navigation bar:

```HTML
<style>
    .nav {
        display: flex;
        justify-content: space-between;
        list-style: none;
        padding: 0;
        margin: 0;
        background-color: #999;
    }

    .nav li {
        margin-right: 20px;
    }

    .nav a {
        color: #fff;
        text-decoration: none;
    }
</style>

<nav>
    <ul class="nav">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>
```

The following example demonstrates how to use flexbox to create a responsive image gallery:

```HTML
<style>
    .gallery {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    .gallery img {
        width: 33.33%;
        margin: 10px;
    }
</style>

<div class="gallery">
    <img src="image1.jpg" alt="Image 1">
    <img src="image2.jpg" alt="Image 2">
    <img src="image3.jpg" alt="Image 3">
    <img src="image4.jpg" alt="Image 4">
    <img src="image5.jpg" alt="Image 5">
    <img src="image6.jpg" alt="Image 6">
</div>
```
The following example demonstrates how to use flexbox to create a flexible grid system:

```HTML
<style>
    .grid {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    .grid > * {
        flex: 1 0 25%;
        margin: 10px;
    }
</style>

<div class="grid">
    <div>1</div>
    <div>2</div>
    <div>3</div>
    <div>4</div>
    <div>5</div>
    <div>6</div>
</div>
```

## Some demonstrations

### To allign nav bar (type-1)

code
```CSS
.parent{
    padding: 10px;
    border: 4px solid indianred;
    display: flex;
    justify-content: center;
    height: 50vh;
    align-items: flex-start;
}

```
image
![flexbox](./src/image3.png)

> Think about `align-items: flex-start;`

### To allign nav bar (type-2)

code
```CSS
.parent{
    padding: 10px;
    /* border: 4px solid indianred; */
    height: 50vh;
    display: flex;
    justify-content: center;
    align-items: center;
}


```
image
![flexbox](./src/image2.png)


### To allign nav bar (type-3)

code
```CSS
.parent{
    padding: 10px;
    /* border: 4px solid indianred; */
    height: 50vh;
    display: flex;
    justify-content: space-between;
    align-items: center ;
}


```
image
![flexbox](./src/image.png)

## Conclusion

Flexbox is a powerful and versatile layout tool in CSS that makes it easy to create complex, responsive layouts with minimal effort. Understanding how to use Flexbox properties such as `flex-direction`, `justify-content`, `align-items`, and others allows you to align and distribute elements in an efficient and flexible way. Whether you're creating a simple navigation bar or a complex grid layout, Flexbox will help you handle various layout challenges with ease.

### Learn More

For more information about CSS Flexbox, visit: 
> - [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
> - [W3Schools](https://www.w3schools.com/css/css3_flexbox.asp)
> - [YouTube (Recommended)](https://www.youtube.com/watch?v=mX-MC_kZZd0&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=31)
