# CSS Selectors  

## What are CSS Selectors?  

CSS **selectors** are patterns used to target and apply styles to specific HTML elements. They allow you to select elements based on their type, attributes, classes, IDs, or relationships with other elements.

Selectors are the foundation of CSS, enabling developers to pinpoint elements and style them as needed.



## Types of CSS Selectors  

### 1. **Universal Selector** (`*`)  

The universal selector applies styles to **all elements** on a page.  

```css
* {
  margin: 0;
  padding: 0;
}
```


### 2. **Element Selector**  

Targets specific HTML elements based on their tag name.  

```css
h1 {
  color: blue;
  font-size: 24px;
}
```

This applies styles to all `<h1>` elements.

### 3. **Class Selector** (`.`)  

Targets elements with a specific `class` attribute. Classes are reusable and can be applied to multiple elements.  

```html
<p class="intro">This is an introduction paragraph.</p>
```

```css
.intro {
  color: green;
  font-style: italic;
}
```

### 4. **ID Selector** (`#`)  

Targets a single element with a unique `id` attribute. IDs must be unique within a page.  

```html
<p id="main-text">This is the main paragraph.</p>
```

```css
#main-text {
  color: red;
  font-weight: bold;
}
```


### 5. **Group Selector**  

Targets multiple elements and applies the same styles to all of them. Elements are separated by a comma `,`.  

```css
h1, h2, p {
  color: darkgray;
  font-family: Arial, sans-serif;
}
```


### 6. **Attribute Selector**  

Targets elements based on their attributes or attribute values.  

```html
<input type="text" placeholder="Enter name">
```

```css
input[type="text"] {
  border: 1px solid black;
}
```


### 7. **Descendant Selector**  

Targets elements that are descendants (nested) of a specified parent element.  

```html
<div>
  <p>This paragraph is inside a div.</p>
</div>
```

```css
div p {
  color: blue;
}
```


### 8. **Child Selector** (`>`)  

Targets **direct child elements** of a parent.  

```html
<div>
  <p>This is a paragraph.</p>
  <span>This is a span.</span>
</div>
```

```css
div > p {
  color: orange;
}
```

### 9. **Adjacent Sibling Selector** (`+`)  

Targets an element that is immediately preceded by a specified sibling.  

```html
<h1>Heading</h1>
<p>This paragraph comes right after the heading.</p>
```

```css
h1 + p {
  color: purple;
}
```


### 10. **General Sibling Selector** (`~`)  

Targets all siblings of a specified element that share the same parent.  

```html
<h1>Heading</h1>
<p>First paragraph.</p>
<p>Second paragraph.</p>
```

```css
h1 ~ p {
  color: brown;
}
```


## Pseudo-Classes and Pseudo-Elements  

CSS also allows more specific targeting using pseudo-classes and pseudo-elements.

### Pseudo-Classes (`:`)  

Targets elements based on a particular state or condition.  

```css
a:hover {
  color: red; /* Change link color on hover */
}
```

### Pseudo-Elements (`::`)  

Targets specific parts of an element.  

```css
p::first-line {
  font-weight: bold; /* Makes the first line bold */
}
```


## Combining Selectors  

You can combine multiple selectors for more precise targeting.  

```css
div.container p.intro {
  color: teal;
}
```

This targets `<p>` elements with the class `intro` that are inside a `<div>` with the class `container`.



## Conclusion  

CSS selectors provide a powerful way to target and style elements in an HTML document. By mastering selectors, you can create highly specific and maintainable styles for your webpages.  
