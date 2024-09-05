# CSS Properties

>CSS properties are the styles that can be applied to elements in an HTML document. They are used to control the layout and appearance of elements, and can be used to create a wide range of visual effects and styles. CSS properties are usually specified using the `style` attribute in HTML elements, or by using an external style sheet.
> ### Examples of CSS properties include:
>* `color`: sets the text color
>* `background-color`: sets the background color
>* `font-size`: sets the font size
>* `padding`: sets the amount of space between an element's content and its border
>* `margin`: sets the amount of space between an element and its parent element
>* `border`: sets the size and style of an element's border
>* `width` and `height`: set the width and height of an element.
>* and more...

## Transform

The `transform` property is used to apply transformations to an element.

### 2D Transformations

* `translate(x, y)`: Moves an element by x and y pixels.
* `translateX(x)`: Moves an element by x pixels horizontally.
* `translateY(y)`: Moves an element by y pixels vertically.
* `rotate(angle)`: Rotates an element by the given angle.
* `scale(x, y)`: Scales an element by x and y.
* `scaleX(x)`: Scales an element horizontally by x.
* `scaleY(y)`: Scales an element vertically by y.
* `skewX(angle)`: Skews an element horizontally by the given angle.
* `skewY(angle)`: Skews an element vertically by the given angle.

### 3D Transformations

* `rotate3d(x, y, z, angle)`: Rotates an element in 3D space by the given angle.
* `scale3d(x, y, z)`: Scales an element in 3D space by x, y, and z.
* `translate3d(x, y, z)`: Moves an element in 3D space by x, y, and z pixels.
* `perspective(n)`: Sets the perspective of an element to n pixels.

```CSS
.box {
    width: 100px;
    height: 100px;
    background-color: rgba(77, 255, 0, 0.7);
    /* opacity: 0.5; */
    transform: scale(2);
    /* transform-origin: 0 0; */
    /* transform: rotate(45deg); */
    /* transform: translateY(50px); */
    transform: translateX(100%);
    transform: translate(100%, 100%);
    /* margin-top: 100px; */
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}
```

> ### Difference between `transform:translate` and `margin`
> * `transform:translate` will not affect the position of other elements, while `margin` will.
> * `transform:translate` will not affect the size of the element, while `margin` will (because it is added to the size of the element).
> * `transform:translate` is more efficient than `margin`, because it does not cause reflow of the document.

## Transition

The `transition` property is used to smoothly change the value of a CSS property over a given duration.
> `hover` is most used transition property

### Transition Property

* `transition-property`: Specifies the property to transition.
* `transition-duration`: Specifies the duration of the transition.
* `transition-timing-function`: Specifies the timing function of the transition.
* `transition-delay`: Specifies the delay before the transition starts.

### Transition Timing Functions

* `linear`: A linear transition.
* `ease`: An ease-in-out transition.
* `ease-in`: An ease-in transition.
* `ease-out`: An ease-out transition.
* `ease-in-out`: An ease-in-out transition.
* `step-start`: A step-start transition.
* `step-end`: A step-end transition.
* `steps(n, start)`: A step transition with n steps and start value.

### Examples of Transition Property

* `transition-property: all;` - Transition all properties.
* `transition-property: background-color, color;` - Transition only background-color and color properties.
* `transition-property: none;` - No transition.
## Opacity
The `opacity` property is used to set the opacity of an element.

* `opacity: 0.5;` sets the opacity of an element to 50%.

### Difference between `opacity` and `transparent`

The `opacity` property is used to set the opacity of an element.

* `opacity: 0.5;` sets the opacity of an element to 50%.

* `opacity` is inherited from parents, but `transparent` is not.
* `opacity` will affect all content of the element, including text, images, etc. but `transparent` will only affect the background color of the element.

## Alpha Channel

The alpha channel is the fourth channel of an image, which represents the transparency of the image.

* `rgba(red, green, blue, alpha)`: Sets the color of an element with an alpha channel.
* `hsla(hue, saturation, lightness, alpha)`: Sets the color of an element with an alpha channel.

## Box Shadow

The `box-shadow` property is used to add a shadow to an element.

* `box-shadow: x-offset y-offset blur-radius spread-radius color;` adds a shadow to an element.
* `box-shadow: inset x-offset y-offset blur-radius spread-radius color;` adds an inset shadow to an element.
```CSS
div {
  box-shadow: 10px 10px 5px 12px lightblue;
}
```

## Text Shadow

The `text-shadow` property is used to add a shadow to text.

* `text-shadow: x-offset y-offset blur-radius color;` adds a shadow to text.
```CSS
h1 {
  text-shadow: 2px 2px 8px #FF0000;
}
```


### Learn More
For more information about CSS Properties, visit: 
> - [W3School Docs](https://www.w3schools.com/cssref/index.php).
> - [YouTube (recommended)](https://www.youtube.com/watch?v=DbSnFAx3Exo&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=25&t=4s)