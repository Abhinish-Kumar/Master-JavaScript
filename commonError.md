```javascript
 let data = [];
      fetch("http://localhost:3300/")
        .then((response) => {
          return response.json();
        })
        .then((jsondata) => data.push(jsondata[0]));
      console.log(data[0]);
```

it will show undefine because 
The fetch function is asynchronous, meaning it runs in the background while the rest of your code continues to execute.Logging Inside .then(): By placing console.log(data[0]) inside the .then() block, you ensure that it runs only after the data has been fetched and added to the array.


```javascript
 let dd;

      let ff = async function apiData() {
        let response = await fetch("http://localhost:3300/");
        let jsondata = await response.json();
        return jsondata;
      };

//ff() return promise so we have to resolve it to get the data from api

      ff()
        .then((data) => {
          dd = data;
          console.log(dd);
         
        })
        .catch((error) => console.error("Error fetching data:", error));
```










