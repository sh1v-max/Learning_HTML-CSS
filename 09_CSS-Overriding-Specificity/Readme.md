# Overriding Specificity

- Specificity order : inline css > id > class > element
- Inline style overwrite every property expect the property on which ```!important``` is there.

- ```!important``` - overwrite all the property.

- How to overwrite ```!important``` ?: It can be overwrite by another ```!important``` only. (by cascade rule) or by increasing the specificity.

```css
li.html#html {
    background-color: darkolivegreen !important;
    color: aquamarine;
}

li {
    background-color: green !important;
    color: aquamarine;
}

li {
    background-color: cornflowerblue !important;
    color: aquamarine;
}
```

NOTE : Refrain from using inline & !important.


### Learn More

For more information about CSS Units, visit: 
> - [YouTube](https://www.youtube.com/watch?v=VresAuRUMO4&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=17)
