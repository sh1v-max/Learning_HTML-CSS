# Cascade in CSS

The cascade is a mechanism that allows multiple stylesheets to be applied to a document and determines the order in which those stylesheets are applied. It is a way to resolve conflicts between different stylesheets and determine which styles should be applied to an element if there are multiple styles that could apply.

The cascade determines the order of stylesheets by looking at the following factors:

- The order of the stylesheets in the document
- The order of the rules within a stylesheet
- The importance of the rule
- The specificity of the selector

The cascade works by applying the stylesheets in the order they appear in the document and then applying the rules within a stylesheet in the order they appear. If there are multiple rules that apply to an element, the rule with the highest importance and specificity will be applied.

## Image
![front-end](./src/image.png)

