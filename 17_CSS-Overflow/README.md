# Overflow in CSS

## What is Overflow in CSS?

Overflow is a CSS property that is used to control how an element handles content that is too large for its specified dimensions. It is used to control the display of content that is larger than its container.

## Values of Overflow

The `overflow` property takes one of the following values:

- `visible`: This is the default value. It displays the content outside the container.
- `hidden`: This value hides the content that is outside the container.
- `scroll`: This value adds a scrollbar to the container so that the user can scroll to see the content that is outside the container.
- `auto`: This value adds a scrollbar to the container if the content is larger than the container. If the content is not larger than the container, then no scrollbar is added.



## Examples of Overflow

### visible
```CSS
<style>
    .visible {
        width: 200px;
        height: 200px;
        background-color: lightblue;
        overflow: visible;
    }
</style>

<div class="visible">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, quidem.
</div>
```

### hidden

```CSS
<style>
    .hidden {
        width: 200px;
        height: 200px;
        background-color: lightblue;
        overflow: hidden;
    }
</style>
<div class="hidden">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, quidem.
</div>
```

### scroll

```CSS
<style>
    .scroll {
        width: 200px;
        height: 200px;
        background-color: lightblue;
        overflow: scroll;
    }
</style>
<div class="scroll">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, quidem.
</div>
```

### auto

```CSS
<style>
    .auto {
        width: 200px;
        height: 200px;
        background-color: lightblue;
        overflow: auto;
    }
</style>
<div class="auto">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, quidem.
</div>
```

### All CSS Overflow Properties

| Property | Description |
| --- | --- |
| `overflow` | Specifies what happens if content overflows an element's box |
| `overflow-wrap` | Specifies whether or not the browser can break lines with long words, if they overflow its container |
| `overflow-x` | Specifies what to do with the left/right edges of the content if it overflows the element's content area |
| `overflow-y` | Specifies what to do with the top/bottom edges of the content if it overflows the element's content area |


### Learn More

For more information about CSS Overflow, visit: 
> - [W3Schools](https://www.w3schools.com/css/css_overflow.asp)
> - [YouTube (Recommended)](https://www.youtube.com/watch?v=berhfH0W4Vw&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=33&ab_channel=AnuragSinghProCodrr)
