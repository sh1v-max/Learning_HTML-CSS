# CSS Units

CSS (Cascading Style Sheets) units are used to define lengths, sizes, and other measurements in a CSS rule. Understanding CSS units is essential for effectively styling web pages. There are two main types of CSS units: **absolute units** and **relative units**. 

This guide explains the different CSS units and their applications.


## 1. **Absolute Units**

Absolute units are fixed in size and do not change based on the environment or parent elements. These units are most commonly used for physical measurements, such as when specifying sizes for print.

### Common Absolute Units:
- **px (pixels)**: 
  - The most commonly used unit. A pixel is the smallest unit of measurement for screen display. It is a fixed size and does not scale with the user's screen or settings.
  - Example: `width: 100px;`

- **pt (points)**:
  - Commonly used in print media. 1 point equals 1/72 of an inch.
  - Example: `font-size: 12pt;`

- **pc (picas)**:
  - 1 pica equals 12 points or 1/6th of an inch.
  - Example: `margin: 3pc;`

- **in (inches)**:
  - An inch is a unit of physical measurement. 1 inch equals 2.54 cm.
  - Example: `width: 2in;`

- **cm (centimeters)**:
  - 1 centimeter equals 10 millimeters.
  - Example: `height: 5cm;`

- **mm (millimeters)**:
  - 1 millimeter is one-tenth of a centimeter.
  - Example: `border-width: 1mm;`


## 2. **Relative Units**

Relative units are more flexible and change based on the context, such as the parent element or the viewport size. These units allow for more responsive and scalable designs.

### Common Relative Units:
- **em**:
  - The `em` unit is relative to the font size of the parent element. It is widely used in typography. For example, if the font size of the parent is 16px, 1em equals 16px.
  - Example: `font-size: 2em;` (This will set the font size to 2 times the parent's font size.)
  
- **rem (root em)**:
  - The `rem` unit is relative to the root element's font size (usually the `<html>` element). It is similar to `em`, but it is always based on the root font size, not the parent element.
  - Example: `font-size: 1.5rem;` (If the root font size is 16px, this will be 24px.)

- **% (percentage)**:
  - The percentage unit is relative to the parent element's size. It's often used for widths, margins, padding, and font sizes. If the parent element is 100px wide, setting an element's width to 50% will make it 50px wide.
  - Example: `width: 50%;` (This will make the element 50% of the parent element's width.)

- **vw (viewport width)**:
  - `vw` is relative to 1% of the viewport width. It is useful for responsive designs and making elements scale with the browser's width.
  - Example: `width: 50vw;` (This will make the element 50% of the viewport's width.)

- **vh (viewport height)**:
  - `vh` is relative to 1% of the viewport height. Like `vw`, it adjusts to the size of the viewport.
  - Example: `height: 100vh;` (This will make the element the full height of the viewport.)

- **vmin and vmax**:
  - `vmin` is relative to the smaller of the viewport's width or height, while `vmax` is relative to the larger of the two.
  - Example: `width: 10vmin;` (The element will take 10% of the smaller dimension of the viewport.)
  - Example: `width: 10vmax;` (The element will take 10% of the larger dimension of the viewport.)

## 3. Font-relative Lengths

Font-relative lengths are relative to the size of the font.

###  em
>- if we want to set font-size using `em` unit,it will consider its parent fontsize (16px by-default) as `1em`, and accordingly it will calculate the font size.
>- but, When using `em` units for properties like width, padding, or margin they are relative to the element's own font size.

###  rem
> - There is another unit called `rem`, it will consider the font size of html/root (inside `HTML:root` tag) as `1rem` (16px by-default), and it will calculate according to that.
> - Let suppose you have set `font-size: 40px;` inside `HTML/:root` tag, than `1rem = 40px`.
> - both `HTML` tag and `:root` tag are same.

### Viewport-percentage Lengths

Viewport-percentage lengths are relative to the size of the viewport.

* `vw`
* `vh`
* `vmin`
* `vmax`

Example: `width: 50vw;`

### Other Lengths

* `ex` (x-height): This unit is used to set lengths as a multiple of the x-height of the font. The x-height is the height of the lowercase letter "x" in the font. For example, `width: 1.5ex;` would set the width of an element to 1.5 times the x-height of the font.

* `ch` (character advance): This unit is used to set lengths as a multiple of the width of the character "0" in the font. For example, `width: 1.5ch;` would set the width of an element to 1.5 times the width of the character "0" in the font.

* `cap` (cap height): This unit is used to set lengths as a multiple of the height of the capital letter "M" in the font. For example, `width: 1.5cap;` would set the width of an element to 1.5 times the height of the capital letter "M" in the font.


## 4. **Which Unit to Use?**

### **When to use Absolute Units:**
- **Print Design**: When designing for print, use units like `in`, `cm`, `mm`, `pt`, and `pc`, which are based on physical measurements.
- **Fixed Layouts**: Use `px` when you need precise control over the size of elements, particularly when designing fixed-width layouts.

### **When to use Relative Units:**
- **Responsive Design**: Use relative units like `%`, `em`, `rem`, `vw`, `vh`, `vmin`, and `vmax` to create responsive layouts that adapt to different screen sizes and user settings.
- **Typography**: Use `em` or `rem` for scalable font sizes, so text remains legible regardless of the user's device or preferences.

### Example: Combining Relative Units for a Responsive Layout

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-size: 16px; /* Base font size */
    }

    h1 {
      font-size: 3rem; /* 3 times the root font size */
    }

    p {
      font-size: 1.5em; /* 1.5 times the parent font size */
    }

    .container {
      width: 80vw; /* 80% of the viewport width */
      height: 60vh; /* 60% of the viewport height */
    }
  </style>
  <title>Responsive Design with Units</title>
</head>
<body>
  <h1>Responsive Heading</h1>
  <p>This paragraph has font-size 1.5 times the parent's font size.</p>
  <div class="container">
    This container has a width and height based on the viewport.
  </div>
</body>
</html>
```

### Explanation:
- **Font size** for `h1` is set to `3rem`, meaning it will be three times the root font size (which is `16px` by default).
- **Font size** for `p` is set to `1.5em`, which means it will be 1.5 times the font size of the parent (in this case, the body).
- The **container**'s width and height are set using `vw` and `vh` units, making it responsive to the viewport dimensions.


## 5. **Conclusion**

- In width & Height calculation, `%`unit is related to parent `width & Height`.
- In padding & Margin calculation, `%`unit is related to parent `Width`.
- In font-size calculation percentage is related to parent font-size.
- Always try to give width value in `px` unit, not in `%` for better practice.
- if you want to give height value in `%` unit, user must give parent height using `px` unit, otherwise it won't work.
- if we want to give padding in `%`, it will calculate it from parent's width.
    
    example-: parent width: 500px; we give 10% padding in his child. so our padding should be 50. 
- Margin behaves same as padding.
- the percentage does not border.
- font-size is calculated based on it's parent font-size.
- `vh` stands for viewport height and `vw` for viewport width. As you can see, the first unit is based on the viewport height, and `1vh` is equivalent to `1%` of the viewport height. same for `vm`. So, `1vw` equals `1%` of the viewport width.



### Learn More

For more information about CSS Units, visit: 
> - [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units).
> - [YouTube (recommended)](https://youtu.be/lZObX0jltus?si=olXfWWW6eg1E2q0p)
> - [YouTube (for em/rem)](https://www.youtube.com/watch?v=tzVHqBFPTEM&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=22)