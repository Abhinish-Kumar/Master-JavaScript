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
When a function executes a javascript engine maintain a stack , in that stack.
When a javascript interpreter go line by line and it encounter the function call it add the function in the call stack and executes it and when it executes teh function it takes it out from the call stack. 
There is  a proper secuence that how the function get executed. 


```javascript
f1(){
......
}
f2(){
......
}
f3(){
......
}

f1();
f2();
f3();

```
CallStack :- take into the call stack , execute f1 and remove it from the call stack. take f2 , execute it ,take it out.take f3 , execute it ,take it out.



```javascript
f1(){
......
}
f2(){
......
f1();
}

f3(){
f2();
}

f3();

```

CallStack :- [f3(),f2(),f1()] first read f1 then pop it out the call stack , then read f2 and pop it out , then read f3 and pop it out.

Note :- f1 can use the variable of f2 and f3. 

This callstack is maintainer by the javascript engine. 

### Synchronous vs Asynchronous propgramming. 
https://www.youtube.com/watch?v=pIjfzjsoVw4&list=PLIJrr73KDmRyCanrlIS8PEOF0kPKgI8jN


## 10 Recursion 

Recursion is a function that refer or call itself. 

Completed in DSA course 

















