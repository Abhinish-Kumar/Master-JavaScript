## 8 IIFE

Immediately Invoked Dunction Expression.

Execute the function immediately after define.
Not need a name.

```javascript
function (){
}
//error:- function statements require a function name

//Group operator :- a bunch of paranthesis. 
(function (){
})();


//IIFE
(function (){
console.log("This is a IIFE function");
})();

```

### Why is it exist?

- external module can not access its variable , it does not polute the global scope.
- Before ES6 we have only var and when we define var outside any function it becomes globally scoped.
- Or another reason is that , if you define a function with a name it exist in a global context. SO there might be chances that some one using  the function with the same name.
- Variable name  with the same name of the function.

## 9 Call stack

First understand `function execution`. 

function Execution Stack = call stack :- a function that comes first executed last. 
When a function executes a javascript engine maintain a stack , in that stack 














