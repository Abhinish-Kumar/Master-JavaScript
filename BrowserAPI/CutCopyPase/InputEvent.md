## Event : Input

The `input` event gets triggered whenever the value in an input box changes. This event happens not only when someone types on the keyboard, but also when the value changes in other ways, like pasting text with the mouse or using voice commands.

Here's an example of how it works:

```html

<input type="text" id="input"> oninput: <span id="result"></span>
<script>
  input.oninput = function() {
    result.innerHTML = input.value;
  };
</script>

```

In this example, whenever the input value changes, the text inside the `<span>` with id "result" will update to show the current input value.


The `input` event is the best option if you want to handle any kind of change in an input field, like in a search bar that updates results as the user types.


If we want to handle every modification of an `<input>` then this event is the best choice.

eg:- searching , for every input. 

However, this event doesn't trigger for actions that don't change the input value, like pressing arrow keys to move the cursor.

Also, you can't use `event.preventDefault()` with the `input` event to stop the value from changing because it runs after the change has already happened. So, it's too late to prevent the change at that point.


### Example :- live search feature on a website


As the user types in the search box, the `input` event triggers and updates the search results dynamically without needing to press enter or click a search button.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Live Search Example</title>
    <style>
        .result-item {
            margin: 5px 0;
            padding: 5px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>

    <h2>Search Items</h2>
    <input type="text" id="searchBox" placeholder="Type to search...">
    <div id="searchResults"></div>

    <script>
        const items = [
            "Apple",
            "Banana",
            "Cherry",
            "Date",
            "Elderberry",
            "Fig",
            "Grape",
            "Honeydew"
        ];

        const searchBox = document.getElementById('searchBox');
        const searchResults = document.getElementById('searchResults');

        searchBox.oninput = function() {
            const query = searchBox.value.toLowerCase();
            searchResults.innerHTML = '';  // Clear previous results

            if (query) {
                const filteredItems = items.filter(item => item.toLowerCase().includes(query));
                filteredItems.forEach(item => {
                    const div = document.createElement('div');
                    div.className = 'result-item';
                    div.textContent = item;
                    searchResults.appendChild(div);
                });

                if (filteredItems.length === 0) {
                    searchResults.textContent = 'No results found';
                }
            }
        };
    </script>

</body>
</html>

```

#### How It Works:

| **Component**    | **Description**                                                                 |
|------------------|---------------------------------------------------------------------------------|
| **Input Field**  | There's an input field where the user can type their search query.              |
| **Search Results** | Below the input field, there's a `<div>` to display the search results.         |
| **Items Array**  | This example uses a simple array of items (fruits) that the user can search through. |
| **oninput Event** | The `input` event on the search box triggers every time the user types something. It filters the items array based on the current input and updates the search results in real-time. |










