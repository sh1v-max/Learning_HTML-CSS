# Cascade, Specificity, and Inheritance in Web Development
## Cascadeing
### The cascade is the algorithm for solving conflicts where multiple CSS rules apply to an HTML element.

 - Cascade is the process of determining which styles will be applied to
an HTML element when there are conflicting styles specified.

 - If two conflicting styles have the same specificity, then the order
of declaration becomes the tiebreaker, and the style declared later will
override the earlier one.

 - The cascade rule considers both specificity and order of declaration,
with specificity taking precedence over order then styles with higher
specificity will be applied.

```css
li {
    background-color: green;
    color: aquamarine;
}

li {
    background-color: cornflowerblue;
    color: aquamarine;
}
```
## Specificity

### In case of conflicting styles, If there are two or more CSS
rules that point to the same element, the selector with the highest specificity value will \"win\", and its style declaration will be applied to that HTML element.

 - Start at 0, universal selector has 0  - id 100  -
class/pseudo-class/attribute-selector 10  - element/pseudo-element 1

 - Internal styles same rules as selectors in external CSS files.

 - Inline style gets a specificity value of 1000

 - If you use the !important rule, it will even override inline styles.

 ```css
 li.html#html {
    background-color: darkolivegreen !important;
    color: aquamarine;
}
li {
    background-color: cornflowerblue !important;
    color: aquamarine;
}

#html {
    background-color: darkmagenta;
}
.html {
    background-color: crimson;
}
 ```
## Inheritance/Multiple CSS files
### All cascade n specificity rules will be applied in files.  
- If selectors has same specificity then styles of later file
will be applied.  
- If selectors has higher specificity in earlier file
and lower specificity in later file, then styles of earlier file will be applied.

```css
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="style2.css">
```

### Learn More

For more information about Cascade, Specificity and Inheritance, visit: 
> - [YouTube (recommended)](https://www.youtube.com/watch?v=eYA9n_lFTNY&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=15)
> - [YouTube](https://www.youtube.com/watch?v=eYA9n_lFTNY&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=16)
