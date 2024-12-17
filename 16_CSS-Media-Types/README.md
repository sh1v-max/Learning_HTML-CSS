# CSS Media Types: A Comprehensive Guide

CSS media types are a crucial aspect of responsive web design. They allow you to apply different styles to a webpage based on certain conditions, such as the type of device, screen size, or orientation. Media types enable the design to adapt to various environments, making websites look good on desktops, tablets, and smartphones.

In this guide, we'll cover the different CSS media types, how to use media queries, and how to apply conditional styles based on the device's characteristics.


## What Are Media Types?

Media types are used to target specific conditions in the user’s environment, such as the device's screen resolution, orientation, or interaction method. A **media query** in CSS allows you to define styles that apply only when the conditions are met, ensuring a responsive design.

### Common Media Types:
- **`all`**: This is the default media type and applies to all devices and viewports.
- **`screen`**: Applies to devices with screens, like desktop monitors, tablets, and smartphones.
- **`print`**: Applies to printed documents or print preview mode.
- **`speech`**: Applies to screen readers or speech-based devices.

### Media Queries

Media queries are used to apply different styles based on different devices or screen sizes. They consist of a media type and one or more expressions that check for the conditions of a particular media feature.

### Basic Syntax of Media Queries:
```css
@media media-type and (condition) {
  /* CSS rules */
}
```

#### The most commonly used media features are:

* `max-width` and `min-width`: To apply styles based on the maximum or minimum width of the screen.
* `max-height` and `min-height`: To apply styles based on the maximum or minimum height of the screen.
* `orientation`: To apply styles based on the orientation of the device.

Example of a media query using `max-width`:


## Media Types in Detail

### 1. **`all`**
The `all` media type applies to all devices, regardless of their properties, and is typically used as the default. It ensures the styles are applied universally across all devices.

```css
@media all {
  body {
    background-color: lightblue;
  }
}
```

### 2. **`screen`**
The `screen` media type targets devices that have a screen, including desktops, laptops, tablets, and mobile phones. This is the most commonly used media type for web design.

```css
@media screen {
  body {
    background-color: lightgreen;
  }
}
```

### 3. **`print`**
The `print` media type is used when the webpage is being printed or previewed for printing. Styles defined for `print` can help optimize the layout for printed documents, such as removing background images or adjusting fonts.

```css
@media print {
  body {
    background-color: white;
    color: black;
  }

  /* Remove navigation links for print */
  nav {
    display: none;
  }
}
```

### 4. **`speech`**
The `speech` media type targets speech synthesis systems or screen readers. It is useful for accessibility purposes, where the page’s content might need to be read aloud to users.

```css
@media speech {
  body {
    font-size: 20px;
    line-height: 1.6;
  }
}
```


## Media Features

Media features are used within media queries to apply styles based on specific conditions like screen width, height, orientation, resolution, etc.

### 1. **`width` & `height`**
These media features allow you to target devices based on their viewport width and height. They are often used in combination with the `max-width` or `min-width` features for responsive designs.

```css
@media screen and (max-width: 600px) {
  body {
    background-color: lightpink;
  }
}
```

- **`max-width`**: Applies styles when the viewport width is less than or equal to the specified value.
- **`min-width`**: Applies styles when the viewport width is greater than or equal to the specified value.
- **`max-height`**: Applies styles when the viewport height is less than or equal to the specified value.
- **`min-height`**: Applies styles when the viewport height is greater than or equal to the specified value.

### 2. **`orientation`**
This media feature checks the orientation of the device, whether it's in portrait (vertical) or landscape (horizontal) mode.

```css
@media screen and (orientation: portrait) {
  body {
    background-color: lightyellow;
  }
}

@media screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}
```

### 3. **`resolution`**
This media feature targets devices with different screen resolutions. It can be used to apply styles for high-DPI screens (e.g., Retina displays).

```css
@media screen and (min-resolution: 192dpi) {
  body {
    background-image: url('high-res-image.png');
  }
}

@media screen and (max-resolution: 96dpi) {
  body {
    background-image: url('low-res-image.png');
  }
}
```

- **`min-resolution`**: For devices with a resolution greater than or equal to a specified value.
- **`max-resolution`**: For devices with a resolution less than or equal to a specified value.

### 4. **`device-width` & `device-height`**
These media features refer to the actual screen size of the device (including physical screen resolution), not just the viewport.

```css
@media screen and (device-width: 375px) {
  body {
    background-color: lightblue;
  }
}
```

- **`device-width`**: The width of the device's screen.
- **`device-height`**: The height of the device's screen.

### 5. **`hover`**
This media feature detects whether the device supports hovering over elements, which is useful for targeting devices with a mouse or trackpad (like desktops and laptops) versus touch-based devices (like smartphones).

```css
@media (hover: hover) {
  .button {
    background-color: blue;
  }
}

@media (hover: none) {
  .button {
    background-color: gray;
  }
}
```

### 6. **`pointer`**
This media feature targets devices based on how they interact with the screen: whether it’s through a precise pointer (e.g., a mouse or stylus) or a coarse pointer (e.g., touch).

```css
@media (pointer: fine) {
  .button {
    font-size: 20px;
  }
}

@media (pointer: coarse) {
  .button {
    font-size: 16px;
  }
}
```


## Combining Multiple Media Queries

You can combine multiple conditions using `and`, `not`, and `only` to create more precise media queries.

### Example: Targeting screen with specific width, orientation, and resolution
```css
@media screen and (min-width: 600px) and (orientation: landscape) and (min-resolution: 192dpi) {
  body {
    background-color: darkblue;
  }
}
```

### Example: Excluding certain devices
```css
@media not all and (max-width: 600px) {
  body {
    background-color: lightgray;
  }
}
```

### Example: Using `only` to target specific devices
```css
@media only screen and (min-width: 1024px) {
  body {
    background-color: lightgreen;
  }
}
```

The `only` keyword prevents styles from being applied to older browsers that do not support media queries.


## Practical Example: Responsive Design Using Media Queries

Here's an example of how media queries can be used to create a responsive layout that adapts to different screen sizes.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
    }

    /* Default styles for larger screens */
    .container {
      display: flex;
      justify-content: space-between;
      padding: 20px;
    }

    .item {
      width: 30%;
      background-color: lightcoral;
      margin: 10px;
      padding: 20px;
      text-align: center;
    }

    /* Styles for small screens (max-width 768px) */
    @media screen and (max-width: 768px) {
      .container {
        flex-direction: column;
        align-items: center;
      }

      .item {
        width: 80%;
      }
    }

    /* Styles for extra-small screens (max-width 480px) */
    @media screen and (max-width: 480px) {
      .container {
        padding: 10px;
      }

      .item {
        width: 100%;
        font-size: 14px;
      }
    }
  </style>
  <title>Responsive Layout</title>
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

## Conclusion

CSS media types and media queries are essential for creating responsive and adaptive web designs. By using media queries, you can customize your website's appearance based on the device's characteristics, such as its screen size, resolution, orientation, or input method. Media queries enable your site to look great on any device, from desktop monitors to smartphones, providing a better user experience across different platforms.

### Learn More

For more information about CSS Media Types and Queries, visit: 
> - [YouTube part 1](https://www.youtube.com/watch?v=AhDPtHd_7i0&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=30&ab_channel=AnuragSinghProCodrr)
> - [YouTube part 2](https://www.youtube.com/watch?v=LJJz1M1qbVE&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=31&ab_channel=AnuragSinghProCodrr)
