# HTML Attributes

## Table of Contents

1. [What are HTML Attributes?](#what-are-html-attributes)  
2. [Syntax of Attributes](#syntax-of-attributes)  
3. [Common HTML Attributes](#common-html-attributes)  
4. [Global Attributes](#global-attributes)  
5. [Custom Attributes](#custom-attributes)  
6. [Conclusion](#conclusion)  


## What are HTML Attributes?

**HTML attributes** provide additional information about an HTML element. They are used to define properties, behavior, or metadata for elements. Attributes are always placed inside the opening tag of an element.

- **Attributes** are written as `name="value"`.  
- They help modify or customize the behavior or appearance of an element.

**Example**:  
```html
<a href="https://example.com" target="_blank">Visit Example</a>
```
- `href` and `target` are attributes.  
- `https://example.com` and `_blank` are their values.


## Syntax of Attributes

HTML attributes follow this syntax:  
```html
<tagname attribute="value">Content</tagname>
```

### Rules for Attributes:
1. Attributes are always in the opening tag.  
2. Attribute names are **case-insensitive** (but lowercase is recommended).  
3. Attribute values are enclosed in **double quotes** (`" "`) or single quotes (`' '`).  
4. Some attributes don’t require values; these are called **boolean attributes** (e.g., `disabled`, `checked`).

## Common HTML Attributes

Here are some of the most commonly used HTML attributes:

| Attribute    | Description                          | Example                                      |
|--------------|--------------------------------------|----------------------------------------------|
| `id`         | Assigns a unique identifier          | `<div id="header">Header</div>`              |
| `class`      | Assigns one or more CSS classes      | `<p class="intro">Welcome</p>`               |
| `style`      | Adds inline CSS styles               | `<p style="color: red;">Red Text</p>`        |
| `title`      | Adds a tooltip on hover              | `<abbr title="HyperText Markup Language">HTML</abbr>` |
| `href`       | Specifies the URL for links          | `<a href="https://example.com">Link</a>`     |
| `src`        | Specifies the source for media       | `<img src="image.jpg" alt="Sample Image">`   |
| `alt`        | Provides alternative text for images | `<img src="image.jpg" alt="An image">`       |
| `target`     | Specifies how to open a link         | `<a href="link" target="_blank">Open</a>`    |
| `disabled`   | Disables an element                  | `<input type="text" disabled>`               |
| `checked`    | Pre-checks a checkbox or radio input | `<input type="checkbox" checked>`            |
| `value`      | Specifies input values               | `<input type="text" value="John">`           |
| `placeholder`| Provides a hint for input fields     | `<input type="text" placeholder="Name">`     |
| `maxlength`  | Limits the input character count     | `<input type="text" maxlength="10">`         |
| `width` / `height` | Sets dimensions for images     | `<img src="image.jpg" width="300" height="200">` |

## Global Attributes

Global attributes can be used with **any HTML element**. Here are some important global attributes:

| Attribute       | Description                               |
|-----------------|-------------------------------------------|
| `id`           | Specifies a unique identifier for the element. |
| `class`        | Assigns CSS class(es) to the element.     |
| `style`        | Inline styling for the element.           |
| `title`        | Provides extra information (tooltip).     |
| `data-*`       | Used for custom data attributes.          |
| `hidden`       | Hides the element from view.              |
| `tabindex`     | Specifies the tab order of elements.      |
| `contenteditable` | Makes the element editable by users.    |
| `draggable`    | Specifies whether an element is draggable.|

**Example**:  
```html
<div id="main" class="container" style="color: blue;" title="Main Section">Hello World</div>
```

## Custom Attributes

HTML allows you to define custom attributes using the `data-*` attribute prefix. These attributes are useful for storing custom data that can be accessed using JavaScript.

**Example**:  
```html
<div data-user-id="12345" data-role="admin">John Doe</div>
```

You can retrieve these values in JavaScript:  
```javascript
let element = document.querySelector('[data-user-id]');
console.log(element.dataset.userId); // Outputs: 12345
```


## Conclusion

HTML attributes are essential for enhancing and controlling the behavior of elements. From defining links with `href` to applying custom styles with `class` and `style`, attributes make HTML versatile and dynamic. Global attributes like `id`, `class`, and `data-*` provide flexibility for modern web development.
