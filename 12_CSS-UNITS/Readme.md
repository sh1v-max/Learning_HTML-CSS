# CSS Units

>CSS units are used to measure the length of an element in an HTML document. They are used to set the width, height, margin, padding, border, and other properties of an element.

### Absolute Units

Absolute units are fixed units that are not relative to the size of the element or the browser window.

* `px` (pixels): This is the most commonly used unit for setting lengths. It is a fixed unit that is equal to one pixel on the screen. For example, `width: 500px;` would set the width of an element to 500 pixels.

* `cm` (centimeters): This unit is used to set lengths in centimeters. For example, `width: 10cm;` would set the width of an element to 10 centimeters.

* `mm` (millimeters): This unit is used to set lengths in millimeters. For example, `width: 10mm;` would set the width of an element to 10 millimeters.

* `in` (inches): This unit is used to set lengths in inches. For example, `width: 5in;` would set the width of an element to 5 inches.

* `pt` (points): This unit is used to set lengths in points. Points are a unit of measurement that is equal to 1/72 of an inch. For example, `width: 72pt;` would set the width of an element to 72 points, or 1 inch.

* `pc` (picas): This unit is used to set lengths in picas. Picas are a unit of measurement that is equal to 12 points, or 1/6 of an inch. For example, `width: 1pc;` would set the width of an element to 1 pica, or 12 points.

### Relative Units

Relative units are relative to the size of the element or the browser window.

* `%` (percentage): This unit is used to set lengths as a percentage of the parent element. For example, `width: 50%;` would set the width of an element to half of its parent's width.

* `em` (font size): This unit is used to set lengths as a multiple of the font size of the element. For example, `width: 1.5em;` would set the width of an element to 1.5 times the size of its font.

* `rem` (root element font size): This unit is used to set lengths as a multiple of the font size of the root element of the document. For example, `width: 1.5rem;` would set the width of an element to 1.5 times the size of the font of the root element.

* `vw` (viewport width): This unit is used to set lengths as a percentage of the viewport width. The viewport is the area of the screen that is visible to the user. For example, `width: 50vw;` would set the width of an element to half of the viewport width.

* `vh` (viewport height): This unit is used to set lengths as a percentage of the viewport height. The viewport is the area of the screen that is visible to the user. For example, `width: 50vh;` would set the width of an element to half of the viewport height.

* `vmin` (viewport minimum): This unit is used to set lengths as a percentage of the minimum of the viewport width and height. The viewport is the area of the screen that is visible to the user. For example, `width: 50vmin;` would set the width of an element to half of the minimum of the viewport width and height.

* `vmax` (viewport maximum): This unit is used to set lengths as a percentage of the maximum of the viewport width and height. The viewport is the area of the screen that is visible to the user. For example, `width: 50vmax;` would set the width of an element to half of the maximum of the viewport width and height.

### Font-relative Lengths

Font-relative lengths are relative to the size of the font.

* `em`
* `rem`

Example: `font-size: 1.5em;`

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

### Learn More

For more information about CSS Units, visit: 
> - [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units).
> - [YouTube (recommended)](https://youtu.be/lZObX0jltus?si=olXfWWW6eg1E2q0p)