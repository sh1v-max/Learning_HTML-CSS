# Introduction to CSS  

## What is CSS?  

**CSS** stands for **Cascading Style Sheets**. It is a stylesheet language used to describe the presentation of HTML documents, allowing developers to control the layout, design, and appearance of web pages.  

While HTML defines the structure and content of a webpage, CSS is used to enhance the visual appeal by adding styles like colors, fonts, spacing, and positioning.

## Why Use CSS?  

CSS provides several benefits:  

1. **Separation of Content and Design**: HTML handles content, while CSS handles the styling, leading to cleaner and more maintainable code.  
2. **Consistency**: By using external stylesheets, you can ensure a consistent look and feel across multiple pages.  
3. **Efficiency**: A single CSS file can be applied to multiple HTML files, reducing redundancy.  
4. **Improved User Experience**: CSS allows for responsive designs that adapt to different screen sizes and devices.  
5. **Customizable Design**: CSS provides powerful styling features like colors, typography, animations, and layouts.


## How Does CSS Work?  

CSS works by **selecting HTML elements** and applying styles to them. It uses **selectors** to target elements and **properties** to define their styles.

### Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>CSS Example</title>
  <style>
    body {
      background-color: lightblue;
      font-family: Arial, sans-serif;
    }
    h1 {
      color: navy;
      text-align: center;
    }
    p {
      color: darkgray;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <h1>Welcome to CSS</h1>
  <p>This is an example of a CSS-styled web page.</p>
</body>
</html>
```

**Output:**  
- The background color is light blue.  
- The heading (`<h1>`) is navy blue and center-aligned.  
- The paragraph (`<p>`) has a dark gray color and 18px font size.  


## CSS Syntax  

CSS follows a simple syntax:  

```css
selector {
  property: value;
}
```

- **Selector**: Targets an HTML element (e.g., `h1`, `p`, `div`, etc.).  
- **Property**: Defines what to style (e.g., `color`, `font-size`, `margin`).  
- **Value**: Specifies the style for the property (e.g., `red`, `20px`, `center`).

### Example:

```css
p {
  color: blue;
  font-size: 16px;
}
```

This code styles all `<p>` elements with a blue color and font size of 16 pixels.


## Ways to Add CSS  

CSS can be applied to HTML in three ways:  

1. **Inline CSS**: Styles are applied directly to HTML elements using the `style` attribute.  

```html
<p style="color: red;">This is a red paragraph.</p>
```

2. **Internal CSS**: CSS rules are defined within a `<style>` tag in the `<head>` section of the HTML document.  

```html
<head>
  <style>
    p {
      color: green;
    }
  </style>
</head>
```

3. **External CSS**: Styles are written in a separate `.css` file and linked using the `<link>` tag.  

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

**Example (`styles.css`):**  
```css
p {
  color: purple;
}
```


## Conclusion  

CSS is a powerful tool for designing and styling web pages. By using CSS, developers can enhance the appearance, improve consistency, and create responsive and user-friendly websites.  

## Image
```Most basic example```

![front-end](./src/image.png)

