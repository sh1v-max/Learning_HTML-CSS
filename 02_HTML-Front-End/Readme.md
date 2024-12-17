# HTML Tags and Elements

## Table of Contents

1. [What are HTML Tags and Elements?](#what-are-html-tags-and-elements)  
2. [HTML Tags](#html-tags)  
   - [Syntax of HTML Tags](#syntax-of-html-tags)  
   - [Types of HTML Tags](#types-of-html-tags)  
3. [HTML Elements](#html-elements)  
   - [Nested Elements](#nested-elements)  
   - [Empty vs. Container Elements](#empty-vs-container-elements)  
4. [Commonly Used HTML Tags](#commonly-used-html-tags)  
5. [Conclusion](#conclusion)



## What are HTML Tags and Elements?

In HTML, **tags** are special keywords surrounded by angle brackets `< >` that define the structure and content of a webpage. When tags are used together with content, they form **elements**. These are the building blocks of any HTML document.

- **Tags** define the meaning and structure.  
- **Elements** represent everything between an opening tag and a closing tag, including the content.



## HTML Tags

HTML tags instruct the browser on how to interpret and display the content.

### Syntax of HTML Tags

An HTML tag usually consists of:

1. **Opening Tag**: Starts with `<` and ends with `>`  
2. **Content**: The actual text or media within the tag  
3. **Closing Tag**: Starts with `</` and ends with `>`  

**Example**:  
```html
<p>This is a paragraph.</p>
```
- `<p>` is the opening tag.  
- `This is a paragraph.` is the content.  
- `</p>` is the closing tag.


### Types of HTML Tags

1. **Paired Tags** (with closing tags):  
   Tags that open and close with content inside.  
   Example: `<h1>Title</h1>`, `<p>Paragraph</p>`  

2. **Self-Closing Tags** (void tags):  
   Tags that don’t require a closing tag.  
   Example: `<img>`, `<br>`, `<hr>`  

## HTML Elements

An **HTML Element** includes everything from the opening tag to the closing tag and the content in between.

**Structure of an HTML Element**:  
```html
<tagname>Content goes here</tagname>
```

### Nested Elements

HTML elements can be **nested** inside one another to build more complex structures.

**Example**:  
```html
<div>
  <h1>Welcome</h1>
  <p>This is a nested paragraph.</p>
</div>
```

- `<div>` is the parent element.  
- `<h1>` and `<p>` are child elements.

### Empty vs. Container Elements

1. **Empty Elements**: These tags do not have content inside.  
   Examples: `<img>`, `<br>`, `<hr>`.  

2. **Container Elements**: These tags wrap around content.  
   Examples: `<div>`, `<p>`, `<h1>`.


## Commonly Used HTML Tags

Here is a list of some commonly used HTML tags:

| Tag       | Description                       | Example                             |
|-----------|-----------------------------------|-------------------------------------|
| `<html>`  | Root of an HTML document          | `<html></html>`                     |
| `<head>`  | Contains meta-information         | `<head><title>My Page</title></head>`|
| `<title>` | Sets the page title               | `<title>Welcome</title>`            |
| `<body>`  | Contains the visible content      | `<body>Content</body>`              |
| `<h1>` to `<h6>` | Headings of different levels | `<h1>Main Heading</h1>`             |
| `<p>`     | Paragraphs                       | `<p>This is a paragraph.</p>`       |
| `<a>`     | Hyperlink to another webpage      | `<a href="url">Link</a>`            |
| `<img>`   | Displays images                   | `<img src="image.jpg" alt="Image">` |
| `<ul>`    | Unordered list                    | `<ul><li>Item</li></ul>`            |
| `<ol>`    | Ordered list                      | `<ol><li>Item</li></ol>`            |
| `<div>`   | A generic container               | `<div>Content</div>`                |
| `<span>`  | Inline container                  | `<span>Inline text</span>`          |
| `<br>`    | Line break                        | `<br>`                              |
| `<hr>`    | Horizontal rule                   | `<hr>`                              |


## Conclusion

HTML tags and elements are essential for structuring and defining the content of a webpage. By using different types of tags, developers can build visually appealing and well-organized web pages. Understanding how to use elements effectively is the foundation of web development.


## A simple project illustration
## Image
![front-end](./images/image.png)

## Live Project Link

[Live Project](https://thefirstwebdev.netlify.app/)
