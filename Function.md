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






















