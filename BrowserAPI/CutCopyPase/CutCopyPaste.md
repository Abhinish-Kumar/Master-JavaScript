# Event : Cut 

These events occur on cutting/copying/pasting a value.

They belong to `ClipboardEvent` class and provide access to the data that is cut/copied/pasted.

We also can use `event.preventDefault()` to abort the action, then nothing gets copied/pasted.

For instance, the code below prevents all cut/copy/paste events and shows the text we’re trying to cut/copy/paste:

```html

<input type="text" id="input">
<script>
  input.onpaste = function(event) {
    alert("paste: " + event.clipboardData.getData('text/plain'));
    event.preventDefault();
  };

  input.oncut = input.oncopy = function(event) {
    alert(event.type + '-' + document.getSelection());
    event.preventDefault();
  };
</script>

```








