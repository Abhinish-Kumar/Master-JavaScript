# All 34 String methods

## Introduction to string

Strings in javascript is a array of characters and its immutable.
Meaning that string methods always return a new string without modifying the original one. 

## When javascript strign behave as a `Object` and `String`

When we create string with "", '', ```` then its datatype is defined as String ,
and when we use `new String("abhinish")` then it behaves like an object. 

```javascript
//dataType is String
const singleQuotes = 'Hello, world!';
const doubleQuotes = "JavaScript is fun!";
const backticks = `You can embed variables like ${variableName}.`;

console.log(typeof a,typeof b,typeof c);
//string string string



//dataType is Object
//String() constructor.
let d = new String("Abhinish");
console.log(typeof d);
//object

```

Not matter you are using which method but at the end of the day javascript convert the string objecct to the object having all the methods and properties of string object. 

## Why we have so many methods to create a string.

1. ```` is used to write a dynamic string value
2. ` "" ` is used  when you want to use `''` within the string
3. ` '' ` is used  when you want to use `""` within the string
 

```javascript

const name = "Alice";
const greeting = `Hello, ${name}!`; // Evaluates to "Hello, Alice!"

const message1 = "She said, 'Hi there!'";

const message2 = 'He replied, "Hello!"';

```


## Properties of String Object

The only property string object has the `Length` property. 



## Methods of String Object
Note:- some methods of string object are at experimental stage and some are depricated. 
















