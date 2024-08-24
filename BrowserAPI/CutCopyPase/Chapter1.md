
 ## Events: change, input, cut, copy, paste

 ### Event: change

 The `change` event triggers when the element has finished changing.

For text inputs that means that the event occurs when it loses focus.

key Points:

- The `change` event only occurs when the element loses focus, not while the user is typing.
- It works with various elements like `<input>`, `<select>`, `<textarea>`, and more.



### Example 1: Text Input

In a text input field, the change event occurs when the user types something and then clicks away from the input field. At button or somewhere else to remove the focus from the input then this function triggers.

 ```html

<input type="text" onchange="alert(this.value)">
<input type="button" value="Click me">

```

Explanation: Start typing in the text input, but the alert will only show up when you click on the button or move the focus elsewhere.

### Example 2: Select Dropdown

When the user selects a different option in a dropdown menu, the `change` event triggers immediately.Value of the select is updated with the selected option.

```html

<select onchange="alert('Selected value: ' + this.value)">
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
  <option value="3">Option 3</option>
</select>


```

Explanation: As soon as you choose an option, the alert displays the selected value.

### Example 3: Checkbox

For checkboxes, the `change` event triggers when the user checks or unchecks the box.

```html

<input type="checkbox" onchange="alert('Checkbox is ' + (this.checked ? 'checked' : 'unchecked'))">
<label>Accept Terms and Conditions</label>

```

Explanation: The alert will indicate whether the checkbox is checked or unchecked as soon as its state changes.

### Example 4: Radio Buttons

For radio buttons, the `change` event triggers when the user selects a different option.

```html

<label><input type="radio" name="gender" value="Male" onchange="alert('Selected: Male')"> Male</label>
<label><input type="radio" name="gender" value="Female" onchange="alert('Selected: Female')"> Female</label>

```

Explanation: The alert displays the selected gender as soon as you choose a different radio button.


### Example 5: Textarea

Similar to text input, the `change` event on a `<textarea>`occurs when the user finishes typing and moves focus away from it.

```html

<textarea onchange="alert('Text area content changed')"></textarea>
<input type="button" value="Click me">

```
Explanation: After typing in the textarea, the alert appears only when you click outside the textarea.


### Summary

1. The `change` event waits until the user finishes interacting and moves focus away.
2. Useful for executing code after user input is finalized.
3. Applicable to various form elements like text inputs, dropdowns, checkboxes, radio buttons, and text areas.











