# CSS Box Model with Block Element

The CSS box model is a concept in CSS that describes how the width and height of an element is calculated. It is composed of four parts: the content area, the padding area, the border area, and the margin area.

- The **content area** is the area inside the element where the actual content is rendered. It is the area that is defined by the `width` and `height` properties of the element.
- The **padding area** is the area between the content area and the border. It is the area that is defined by the `padding` property of the element.
- The **border area** is the area between the padding and the margin. It is the area that is defined by the `border` property of the element.
- The **margin area** is the area outside the border. It is the area that is defined by the `margin` property of the element.

```CSS
.one {
    background-color: aquamarine;
    width: 300px;
    padding: 24px;
    border: 10px solid teal;
}
```

![CSS Box Model](./src/box.png)

### What is Block Element:

> A block element is an HTML element that takes up the full width available and starts on a new line. It is an element that is not an inline element. It is an element that is used to group other HTML elements together. It is an element that is used to add structure to the page, to group related content together, and to apply styles to a group of elements. It is an element that is used to create a container for other elements, such as a header, footer, or sidebar.


The total width and height of an element is calculated by adding up the widths and heights of the content area, padding area, border area, and margin area.

For example, if an element has a width of 300px, a padding of 20px, a border of 10px, and a margin of 30px, the total width of the element would be 300px + 20px + 10px + 30px = 360px.

The box model can be changed by using the `box-sizing` property. The default value is `content-box`, which calculates the width and height of the element as the content area plus the padding and border areas. The `border-box` value calculates the width and height of the element as the content area only, and the padding and border areas are subtracted from the width and height.

- _To avoid overflow you should always set max-with not absolute width._

- _We use padding because to generate space around an element's content._ 

- _Border by default color set as our text color, but we can overright it._

- _when we add padding & border the overral width of the box will increse , to avoid that we can use one property (box-sizing: border-box;)._

- _Margin will not affect our inner content. it apply in the outside of the box._

- _for making circle using border radius property, user should must apply width & height._

- _The outline is drawn outside the element's border, and may overlap other content. Also, the outline is NOT a part of the element's dimensions; the element's total width and height is not affected by the width of the outline._

- _box-sizing is used to include the padding and border in an element's total width and height._

- _want to set the width and height of an element and not have to worry about the padding and border also being added to the width and height._

- _It is also useful when we want all elements to have the same box model, regardless of their border and padding._

## Working with CSS Styles

``` CSS
.two {
    background-color: #361601;
    width: 300px;
    height: 300px;
    padding: 25px;
    border: 8px solid rgb(225, 0, 255);
    margin: 40px;
    border-radius: 50%;
    overflow: hidden;
    outline: 15px solid #15ff00;
}

img{
    width: 125%;
    height: 125%;
    margin-top: -24px;
    margin-left: -25px;
    background: linear-gradient(to bottom right, #3700ff,#ff2eff);
    
}
```
### Image
![box-model](./src/image.png)


### Learn More

For more information about CSS Box Model with Block Element, visit: 
> - [YouTube Part-1 (recommended)](https://www.youtube.com/watch?v=Ab5ztcNsanc&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=18)
> - [YouTube Part-2 (recommended)](https://www.youtube.com/watch?v=1mPG8o4jSZI&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=19)
> - [YouTube Part-3](https://www.youtube.com/watch?v=JnY16NvJbXE&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=20)
