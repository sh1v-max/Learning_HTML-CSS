# FORM in HTML

An HTML form is used to collect user input. The user input is most often sent to a server for processing.

The HTML `<form>` element is used to create an HTML form for user input

```HTML
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" value="John"><br><br>
  <input type="submit" value="Submit">
</form>
```

## Input Types

| Type | Description |
| --- | --- |
| `<input type="text">` | Displays a single-line text input field |
| `<input type="radio">` | Displays a radio button (for selecting one of many choices) |
| `<input type="checkbox">` | Displays a checkbox (for selecting zero or more of many choices) |
| `<input type="submit">` | Displays a submit button (for submitting the form) |
| `<input type="button">` | Displays a clickable button |

### Input types in Form

* `<input type="button">`: A push button with no default behavior.
* `<input type="checkbox">`: A check box. It is used to select or deselect an option.
* `<input type="color">`: A color picker.
* `<input type="date">`: A date picker.
* `<input type="datetime-local">`: A date and time picker.
* `<input type="email">`: A field for an e-mail address.
* `<input type="file">`: A file select field. It is used to select a file from the user's computer.
* `<input type="hidden">`: A hidden field. It is not visible to the user, but the value is sent to the server.
* `<input type="image">`: An image button. It is used to submit a form.
* `<input type="month">`: A month and year picker.
* `<input type="number">`: A numerical input field.
* `<input type="password">`: A password field. It is used to enter a password.
* `<input type="radio">`: A radio button. It is used to select one of many options.
* `<input type="range">`: A slider control. It is used to enter a numerical value within a range.
* `<input type="reset">`: A reset button. It is used to reset all form values to their default values.
* `<input type="search">`: A search field. It is used to enter search keywords.
* `<input type="submit">`: A submit button. It is used to submit a form.
* `<input type="tel">`: A telephone number field.
* `<input type="text">`: A single-line text field. It is the default value of the type attribute.
* `<input type="time">`: A time picker.
* `<input type="url">`: A URL field. It is used to enter a URL.
* `<input type="week">`: A week and year picker.

### Attributes

| Attribute | Description |
| --- | --- |
| `accept-charset` | Specifies the character encodings used for form submission |
| `action` | Specifies where to send the form-data when a form is submitted |
| `autocomplete` | Specifies whether a form should have autocomplete on or off |
| `enctype` | Specifies how the form-data should be encoded when submitting it to the server (only for method="post") |
| `method` | Specifies the HTTP method to use when sending form-data |
| `name` | Specifies the name of the form |
| `novalidate` | Specifies that the form should not be validated when submitted |
| `rel` | Specifies the relationship between a linked resource and the current document |
| `target` | Specifies where to display the response that is received after submitting the form |

### Form Elements

* `<input>`: Used to create interactive controls for web forms.
* `<label>`: Used to add a label to a form control.
* `<select>`: Used to create a drop-down list of options.
* `<textarea>`: Used to create a text area for entering large amounts of text.
* `<button>`: Used to create a button for a form.
* `<fieldset>`: Used to group related form controls together.
* `<legend>`: Used to add a legend to a `<fieldset>`.
* `<datalist>`: Used to create a list of options for an `<input>`.
* `<output>`: Used to display the result of a calculation or user action.
* `<option>`: Used to create an option in a `<select>`.
* `<optgroup>`: Used to group related options together in a `<select>`.



## Image
![front-end](./images/image.png)
