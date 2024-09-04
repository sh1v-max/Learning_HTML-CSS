# CSS Box Model with Inline Elements

### What is Inline Element:
>Inline elements are elements that only take up the space of their content and do not force a line break. They are used to wrap a small section of text or an image.
>
>it does not show same behaviour as block element

## Example

### Image

![box-model-inline](./src/image.png)

### Code
```CSS
p{
    background-color: greenyellow;
    width: 300px;
    height: 100px;
    padding: 25px;
    box-sizing: border-box;
    border: 10px solid green;
    margin: 25px;
}

.html{
    background-color: skyblue;
    width: 300px;
    height: 100px;
    margin: 25px;
}
```
_Now see the image and code:_

> - `.html` which is a `class` of `span`(an inline element) and is not following Box Model orders.
> - its not following measurments for `height` and `width` as given values:

### ***you can apply ```display: block;``` to make inline element follow the box model order***

```CSS
display:  inline-block;
width: 300px;
height: 100px
```
### Types: Replaced and Non-Replaced Inline Elements

Inline elements can be replaced or non-replaced. Replaced inline elements are those whose content is replaced by an external object such as an image or a plugin. Non-replaced inline elements are those where the content is not replaced by an external object.

#### Replaced Inline Elements

> they follow Box Sizing order, ie `Height` and `Width`

Example of replaced inline elements are:

 `<img>`,`<iframe>`,  `<input>`, `<textarea>`, `<select>`, `<object>`, `<embed>`, `<video>`, `<audio>`

#### Non-Replaced Inline Elements
> they dont follow Box Sizing order, ie `Height` and `Width`

Example of non-replaced inline elements are:

 `<span>`, `<a>`, `<label>`, `<button>`, `<abbr>`, `<cite>`, `<code>`, `<var>`, `<dfn>`, `<kbd>`, `<q>`, `<samp>`, `<sub>`, `<sup>`, `<em>`, `<strong>`, `<mark>`, `<small>`, `<i>`, `<b>`, `<u>`, `
