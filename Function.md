# Javascript Functions

Concepts >>>> syntax

## Table of Contents

1. [Function Fundamentals](#1-function-fundamentals)
2. [Function Declarations](#2-function-declarations)
3. [Function Execution](#3-function-execution)
4. [Call Stack](#4-call-stack)
5. [Arrow Functions](#5-arrow-functions)
6. [Nested Functions](#6-nested-functions)
7. [Scope](#7-scope)
8. [Closure](#8-closure)
9. [Callback Functions](#9-callback-functions)
10. [Higher-Order Functions](#10-higher-order-functions)
11. [Pure Functions](#11-pure-functions)
12. [IIFE](#12-iife)
13. [Recursion](#13-recursion)

## 1. Function Fundamentals

To cook food call to friend for food recipie step by step to cook the food at your home and your food is ready. 
Javascript allow us to write a block of code once and read it every time whenever we need it. Reusable block of code is called a function. Write a block of code give it a name and you can use this whole block of code by calling its name only. 
We are reducing the line of codes , and we are using the same code again and again. If we have  a bug , then we only need to change at single place in our function.
In javascript we have functions without name also. The purpose of the name is that somebody can call us by that name . If we call the function with its name then function will say that heyy i am here with this lines of code , come and execute these lines of code.

### Key Terminologies

1. **Functions/Methods**
2. **Declaration/Definition**
3. **Arguments/Parameters**
4. **Callback/Higher-Order Functions**



### 2. Function Declarations

Funcyion holds a bunch of code that we can call again and again with its name. 

To declare or define a function 

`Declaration/Defination` both are same for functions. 
Means creating a function with bunch of logic. 


```javascript
//function here is a keyword 
function printMe(){
console.log("printing........");
}

//This is called as function defination and function declaration.

//call this function , just type its name and add () to call it.
//with `name` of a function it just print the body of a function only , and by adding `name()` it executes the function and give output instead of giving the body.

```

### 3. Parameter 

```javascript

function printThis(param){
console.log(param);
}

//whatever you put in this paranthesis is called parameters.
//you can pass n number of parameters

//call function with value
//this value get maped with the parameters of function
printThis("abhinish);
```

Anything inside paranthesis of function defination is called parameter. And the actual value that you pass at the calling time of that function is called as argument. 


### 4. Function ` Expression `

Whe you pass a value to a variable the this is called as `expression`

```javascript

//expression
const count = 100;

//function expression
//function assigning to a variable
//printMe define the function
//printMe() calls the function
const printMe = function(){
console.log("print");
}


function printMe(){
console.log("print");
}

```

These are the two ways to create a function one with a function and another without a function. 



# Declaration vs Expression

In JavaScript, function declarations and function expressions are two ways to define functions, and they have some key differences:

## 1. Function Declaration
A function declaration defines a named function that can be called before it is defined in the code.


```javascript

function functionName(parameters) {
    // Function body
}

```
```javascript
greet(); // Output: Hello, world!
function greet() {
    console.log("Hello, world!");
}
greet(); // Output: Hello, world!

```

### Key Characteristics:

1. Hoisting: Function declarations are hoisted to the top of their scope. This means you can call the function before the line where it's declared in the code.
2. Naming: The function must have a name.


## 2. Function Declaration

A function expression defines a function as part of a larger expression, typically assigned to a variable. This function can be named or anonymous.

```javascript

const functionName = function(parameters) {
    // Function body
};

```

```javascript

//Anonymous Function Expression

greet(); //ReferenceError: Cannot access 'greet' before initialization
const greet = function() {
    console.log("Hello, world!");
};
greet(); // Output: Hello, world!

//Does not have a name; useful when the function is only needed for a specific context.



//for recursion
// Named function expression assigned to a variable
const factorial = function fact(n) {
    if (n <= 1) {
        return 1;
    } else {
        return n * fact(n - 1); // Using the function's own name for recursion
    }
};

// Calling the function
console.log(factorial(5)); // Output: 120

//Has a name that can be used internally within the function; useful for recursion or when the function needs to reference itself.
```




### Key Characteristics:

1. Hoisting: Function expressions are not hoisted. The function can only be called after the line where it is defined.
2. Naming: The function can be anonymous or have a name (though anonymous functions are more common).
3. Flexibility: Function expressions can be used as arguments to other functions, returned from other functions, and assigned to variables. Thats why it is also called as `"first-class functions"`



# Chapter 2

## 1. Function Execution

```javascript
let p = x();

//p store the executed output of x function. that we can use somewhere
//when x() does not return any thing but it has line to log some value
// in that case it return `undefined`
//return thing is not defined yet.

```


```javascript
//1st way
function sum(a,b){
return a + b;
}

sum(4,5); //9

//2nd way
function sum(a,b){
let ret = a + b;
return ret;
}

```


## Default Parameters

When you not pass a value to parameter it is `undefined` we know that.

```javascript
function add(x,y){
return (x*y);
}

add(5,5); //25

add(5);// NaN (not a number)

//undefined is not a number 

```

Solution :- set some default value , to avoid failure

```javascript
function add(x=0,y=0){
return x*y;
}

console.log(add(5,5)) //25

console.log(add(5)) //0

```
In this way you can override the undefied value to of the parameters , be setting a default parameter. 


## 2. Rest parameters

Rest parameters allow a function to accept any number of arguments.

```javascript
//rest at last only
//a function only can have one rest parameter

function collectThings(x,...y){

}

//rest means , rest of it whatever is left include all
//Thats why we define at the end 


function collectThings(x,...y){
console.log(x); //map 1st argument 
console.log(y); //store all the rest argument (in array)
}

collectThings(1,2,3,4,5);


//x= 1
//y=[2,3,4,5]

```

Take rest array and loop to a particular function

eg:-Summing Numbers

```javascript

function sumAll(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}

console.log(sumAll(1, 2, 3));        // Outputs: 6
console.log(sumAll(5, 10, 15, 20));  // Outputs: 50
console.log(sumAll(7));              // Outputs: 7

```

eg:- Combining Arguments

```javascript

function greet(greeting, ...names) {
    return `${greeting} ${names.join(", ")}!`;
}

console.log(greet("Hello", "Alice", "Bob", "Charlie"));
// Outputs: "Hello Alice, Bob, Charlie!"

```
the rest parameter provides a powerful and flexible way to handle function arguments, making your functions more adaptable and easier to work with. like :- When writing functions that may accept an unknown number of arguments., Variable inputs.

## 3. Arrow function (fat arrow syntax)

to write less amount of code.

```javascript
const add=function(x,y){
return x+y;
}

//arrow function
const add=(x,y) => {
return x+y;
}

//for one line funcion
const add = (x,y) => x+y;


//With one parameter
const add = x => x+x;

```

Because of its short syntax we use this arrow funciton.

## 4. Nested Functions
What does nesting mean? 
First thing to understand about closure in jvascript function.

```javascript
function outerFunction() {
    console.log("Outer");

    // Nested function
    function innerFunction() {
        console.log("Inner");
    }

    // Calling the nested function
    innerFunction();
}

// Calling the outer function
outerFunction();


//Outer
//Inner
//when invoke inner function

```

The outer function call read the defination of it , then it read the nested function and store its defination in its scope and when it encounter its call it return the output of it. 


####  Key Characteristics of Nested Functions

1. Scope Access: A nested function has access to the variables and parameters of its containing (outer) function. This is due to JavaScript's lexical scoping.
2. Encapsulation: Nested functions help in encapsulating functionality. The inner function is only accessible within the outer function, which can help in keeping the global scope clean.

```javascript

function calculator(a, b) {
    function add() {
        return a + b;
    }
    
    function subtract() {
        return a - b;
    }
    
    return {
        sum: add(),
        difference: subtract()
    };
}

const result = calculator(5, 3);
console.log(result.sum);        // Outputs: 8
console.log(result.difference); // Outputs: 2

```

3. Closures: Nested functions often create closures. A closure is a function that retains access to its lexical scope, even when the outer function has finished execution.

```javascript
function outerFunction() {
    const outerVar = 'I am outer';

    function innerFunction() {
        console.log(outerVar); // Can still access outerVar
    }

    return innerFunction;
}

const myInnerFunc = outerFunction();
myInnerFunc(); // Outputs: "I am outer"

```
## 4. Function Scope
Pohoch of a function

Nested function and Scope is  related to each other. What are the vaiables that a nested function can access. 

1. In a javascript file by default funcion is running globally , file is  a big box.
2. funcion is a another box in the bigger box of that file.
3. Two rules of closure (`1. variable inside a funcion is not accessed by anywhere outside the funcion, its protected, no one ouside the funcion can access its vaiable`) (`2. as opposite to it , a funcion can access all the variables inside the scope it is defined`)
4. This two rules are valid for nested functions also. 


```javascript

function  deSomething(){
let x = 10;
const y = 20;
var z = 30;

console.log(x,y,z);
}

deSomething() //10 20 30

// try to access vaiable of this funcion

console.log(x); //ReferenceError: x is not defined
console.log(y); //ReferenceError: y is not defined
console.log(z); //ReferenceError: z is not defined

//1st principle satisfied that you can not access the variable of a funcion outside of a function, it will show reference error.

```

```javascript

let x = 10;
const y = 20;
var z = 30;

function  deSomething(){
console.log(x,y,z); 
}
deSomething(); // 10 20 30

//2nd principle satisfied that a function can access the variable of its outer scope.

```


## 5. Closures

This is a comples javascript topic and most asked interview question. 
Learn by connecting dots.

1. Take two nested funciion (inner or outer).
2. Outer variable is accessible by the inner funcion, but inner vaiable is not accessible by the outer variable.
3. The nested funcion is a `closure`
4. Defination (A closure is a function that can have free variables together with the environment  that can run that variable)
5. SO that we call that the inner funcion is called as closure. Its a packed that wraps all tht things.
6. The cloud of a outer funcion is used by the inner function but the outer function can not use the inner function variable (inner function + its cloud == closure), or my defination is that ,` the outer function provide a environment for the servival of inner function is called as closure`;

```javascript
function outer(x){
function inner(y){
return x*y;
}
return inner;
}

const outerReturn = outer(10);
//ineer funcion returned 
//outer is over

//The 10 is also live with inner function after the execution of outer funcion , because its closure that maintain the environment for inner function with required data for inner funcion. 

```
it is used to preserver the variable of outer function.


### What is a Closure?
A closure in JavaScript is a feature where an inner function has access to the outer (enclosing) function's variables and parameters even after the outer function has returned. In simpler terms, a closure allows a function to remember and access its lexical scope even when it's executed outside its original scope.

### Real-World Analogy
Think of a closure like a backpack. When you go hiking (execute a function), you pack some supplies (variables) in your backpack. Even after you leave your house (the outer function finishes executing), you still have access to the supplies in your backpack (the inner function retains access to the outer function's variables).


### Why are Closures Useful?
Closures are powerful because they allow for:

1. Data Privacy: You can create private variables that can only be accessed by specific functions.
2. Stateful Functions: Functions can maintain state between executions.
3. Function Factories: You can create functions that generate other customized functions.


eg:- 
```javascript
function greeting(name) {
    return function(message) {
        console.log(`${message}, ${name}!`);
    };
}

const greetJohn = greeting('John');
greetJohn('Hello'); // Outputs: "Hello, John!"
greetJohn('Good morning'); // Outputs: "Good morning, John!"

```
58. 


#### Lexical Scope
In JavaScript, functions are executed using the scope in which they were defined, not where they are executed. This is known as lexical scope.

```javascript
function outer() {
    const outerVar = 'I am outside!';

    function inner() {
        console.log(outerVar);
    }

    inner();
}

outer(); // Outputs: "I am outside!"

```
Closures are commonly used in asynchronous 

```javascript

function delayedGreeting(name) {
    setTimeout(function() {
        console.log(`Hello, ${name}!`);
    }, 1000);
}

delayedGreeting('Alice'); // Outputs: "Hello, Alice!" after 1 second

```

## 6. Callback function

Call me back some point of time.


In javascript function is `1st class citizen` , means we can create a function, we can assign a funcion to variable,  we can pass functin as parameter. 

```javascript

function foo(bar){
bar(); /callback
}

foo(function(){
console.log("bar"); //anonymus function (function without name)
});

foo(function(){
console.log("this is another bar"); //anonymus function (function without name)
});

```

The function that we pass as a argument to another function and use that funcion then that function is called as `callback` function. 

```javascript
//two condition to call bar

function foo(bar){
if(isNight){
bar();
}
if(isDrinkOverCheck Online){
bar(); //calling it back at certain condition
}
}
```

Its so powerful because you can use any function to pass as argument and can call it back at any condition.

Eg:- pizza hub. order pizza.


## 6. Higher Order Function

A higher order function is a regular function that takes one or more function as an argument and return a function as a value. 
COnditions for Higher Order Function

1. It takes one or more functions as argument
2. It may return a fucntion

A call back function is a function which take a function as  an argument based on certain condition. what ever function we pass in a function as as argument it is going to invoke that function inside. (call this function when condition satisfied)


Callback and HOF are not exactly same , because in callback function its not mendatory for a function to return a function. And when a funciton returns a function then it is called as higher order function.


```javascript

function getCapture(Camera){
camera(); // callback function
}
getCapture(function(){
console.log("canon");
})

```

```javascript

function returnFn(){
return function(){
console.log("returning")
}
}

//1st way to execute this function
const fn = returnFn(); //return a function

fn() //execute the returned function

//2nd way
returnFn()();

```
`map filter reduce ` all are HOF you write a function in fileter for condition. 


Lets deep dive into it.

A Higher order function is a function that takes a function as an argument and return a function as return value. And it can do any one of then. Then it is called as higher order function. 

```javascript

//passing function as argument
getCapture(function(){
return "canon";
}
)

//returning a function as a value
function returnFn(){
return function(){
console.log("hi);
}
}

```

How It is useful 


```javascript
//Increment each element in array by 3
function incrArr(arr,n){
let result = [];

for(const elem of arr){
result.push(elem + n);
}
return result;
}

incrArr([1,2,3,4,5],2);

//output :- [ 3, 4, 5, 6, 7 ]

```

1. You can use decrement also.
2. For multiply to each element you need to change the function.

Its not good , because we are repeating the code.

Use Higher Order Function(create a `pure function`);

**Pure Functions are the function that return same output for the same input.**


```javascript
//pure functions
function decr(num,pad){
return num - pad;
}
function mul(num,pad){
return num * pad;
}
function incr(num,pad){
return num + pad;
}

//Write higher order function
//a function that take function as an argument

function smartOperation(data,op,pad){
//op is operation - + or function
//pad value to increment or decrement 
let result = [];

for(const elem of data){
result.push(op(elem,pad)) //pass element and data
//op is any function that you pass as argument
}
return result;
}

//call the smart function
let data=[1,2,3,4];
console.log(smartOperation(data,incr,4))

//[ 5, 6, 7, 8 ]
```

We are just taking the array and inside function we are calling the callback function with each value of the array and that callback function return the output and here we are saving the return value of the callback in to the result array.


Just by passing different callback you can change the functionality of the smartFunction.

What ever the operation you want to do with your  array you cna do so. 
These concept is used by array methods , Thats why we call `map,filter,reduce` are higher order functions.  

The condition that you pass in filter is a function.

```javascript
data.filter(function(elem,index){
return elem > 10;
})
```

It accepts a function that why its HOF.


NOte:- Highere Order function is not same as CallBack functions. Callback functions are the functions that we pass as an argument to another function. (at the function defination, then called as callback function) (and when you pass a function at calling time then its called as HOF). 

eg: smartOperation is a higher order function thats excepting a function as an argument , and the function we are passing is called as callback function.

```javascript

//smartOperation a HOF
//pad is CallBack function
function smartOperation(data,op,pad){
...
...
}

```
They both are related but they are not same. 













