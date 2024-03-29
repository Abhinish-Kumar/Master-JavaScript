# Master-JavaScript(advance level)

This is a master course of JavaScript. In this course you can learn how the things works in JavaScript when to use and how to use it. All the topics are in readme format.











# Javascript Essentials (Modern Javascript)

1. HTML is the Language of Web Content.
2. CSS is the Language of Web Style.
3. JS is the language of That brings all these together.

##### Javascript is used as
1. Vanilla JavaScript
2. ECMAScript
3. TypeScript
4. ES6
5. ES2015
6. CoffeeScript
7. Node js
8. WebPack
9. JSX
10. Gulp
11. Babel
12. Web Pack
13. Angular
14. React
15. Vue.js

Npm,Web Pack,Gulp are help applications.

#### Toolsa for Working with Javascript

1. Modern Brower
2. Code editor
3. Live server
4. The browser console


#### ESlint and Prettier
Install both on vscode

1. Eslint:- Helps automatically detect coding errors and can do basic cleanup automatically.
2. Prettier:- helps automatically cleanup your formatting.
Both require Node.js,>Run npm install in terminal of vscode.
file>prefferences>setting>search formatonsave>tick it.

#### Js basics
1. Use comments to describe your code 
```javascript

//Single line comment
/*
Multiline comment
*/

/**
 * 
 * 
 * 
 * 
 * 
 * 
 */
```

2. Define a functon and variable at top 
3. Use double or single quatation for string.
4. Semicolons are not required.
5. Check Tab size in vscode bottom ribbon.
6. Use white space to make your code more redable browser dont have any issiue with white spaces.
7. Comments are also used in debugging.
8. Select code press CTRL + / (for comment).


#### Js in html document

We have to put the js file at the bottom so that it can access the html elements easily and manupulate them.But when we put it on head section compiler runs the html line by line and if it runs the js file it does not get the body element and show error to the console because our body is not loaded yet.

#### Moder javascript loading 
If you want to use JS in head section use "asunc" and "defer".Normally if you put the js in head section.

1. HTML parsing.
2. HTML parsing stop + Javascript Downloaded.
3. Html parsing stop + Javascript Executed.
4. Javascript Execuition Complete + Remaining HTML content is loaded.

The above is called as Content and rendering blocking.Because it blocks the rendering of HTML Content it slow down the website.

#### Async
Browser downloads js in parallel while HTML renders.When JS is fully loaded,rendering stops while JS is executed.

1. HTML parsing + download JS.
2. Stop parsing HTML + executing JS.
3. Start parsing HTML.

#### defer
Browser downloads JS in parallel while HTML renders,then defer execution of JS until HTML renders in complete.

1. HTML parsing + download JS.
2. When HTMl parsing complete then at last start execuiting Js.

Async/defer is the standard way to load js today.
Only use render  blocking when you have a specific reason.Loading JS in the footer is now an anti-pattern.



### Javascript Modules
Js modules allows us to break pieces of code from a javascript file and place it into separate file and then import them back into the original file again.

```javascript
import person from "./info.js";
console.log(person);
```
```javascript
//info.js

const person={
//person information
};

export default person;
```
You can not get person object in console because person object is only available for that info.js file.


### Object
1. With javascript we are working with objects that are based on prototypes.
2. JS deals with objects as we deals with the real world objects like a car or a bag all the object has its own property.
3. Each object is a unique instance of an object prototype.
4. like all the bags have two straps are common in all the bags and all are open at top.
5. Methods:-property changing features inside objects.
6. Eg :- same method to open and close the bag.
7. Objects  can contain the other object.


Javascript object is the collection of data and properties and methods that describes the objects and what it can do.

```javascript
const obj={};
//curly brackets define the object

const obj1={
key:"value", //property defined as key-value pairs.
}
```
1. values can be any data type.
2. Properties can nest sub-objects with their own properties.
3. Methods are properties containing function.
4. This keywords simply refers to the current object.



#### Object container

The object container somewhere to live.Foe this we use a container called variable or constant variable.

```javascript
const box={}
```

const is the constant variable. (box)   is the name of the container. Whaterver is at RHS is placed at that box container.

#### Objects are typically constants

We can change the properties of the object inside the container.We can't remove or replace object from the container.

```javascript
const box={name:"magic box"}

box=5;//error its a consant

box.inside="apple"

console.log(box);

//{name: 'magic box', inside: 'apple'}


```

#### Object properties

1. Object properties are defined using a collon separated key-value pair.
2. Key or name can be any string and it is placed at the left and the value can be any data-type.
3. Name can contain letter,digit,$,underscore.


#### Accessing Object 

```javascript

const box={};
console.og("This is a box:",box);

```


#### Accessing Object Properties

1. Dot notation:-is called dot-notation because you use the dot to separate the different property.

```javascript
const car={
    name:"bmw"
}

console.log(car.name);
```

2. Bracket notaion:-it allows to use more advance things and give us more control to access the property.

```javascript
const car={
    name:"bmw",
    info:{
        color:"red"
    }
}

// 1st use
console.log(car["name"]);//BMW

//2nd use (we can use the variable to get the property of an object

let n="name";
console.log(car[n]);//BMW

console.log(name["info"]["color"]);//red
```

```javascript
//3rd use (We can use key of the property which not follow the naming convention).
const person={1:"first"}
console.log(person["1"]);//first
```


#### Object methods
Object can contain contain their own function.These function typically perform actions on properties of object and when a function is inside in a object is called as method.

There are two ways to define a method.

```javascript
const car={
    name:"Sujuki",
   firstMethod:function(a){
       console.log(this.name)
   }
}
car.firstMethod()//Sujuki
```

or

```javascript
const car={
    name:"Sujuki",
   secondMethod(a){
       console.log(this.name)
   }
}
car.secondMethod()//Sujuki
```
Example1.

```javascript
const car={
    name:"Sujuki",
   firstMethod(newName){
       this.name=newName;
   }
}

console.log(car.name)//Sujuki

car.firstMethod("BMW");

console.log(car.name)//BMW

```
The value is changed only on the user browser at that moment.It is used to control somethin like in game to move front and back by pressing keys.
Example2.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      body {
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      #box {
        width: 300px;
        height: 300px;
        background-color: pink;
        border: 1px solid black;
      }
    </style>
  </head>
  <body>
    <div id="box"></div>
    <script src="script.js"></script>
  </body>
</html>

```

```javascript
// Select the box element
var box = document.getElementById("box");
var width = 0;
var height = 0;

// Add an event listener to the document object
document.addEventListener("keydown", function (event) {
          console.log(event);
  // Check if the right arrow key was pressed
  if (event.keyCode == 39) {
    // Change the background color of the box
    // Increment the margin value by 100
    width += 100;
    // Set the new margin value to the box element
    box.style.width = width + "px";
  }
  if (event.keyCode == 37) {
    // Change the background color of the box

    
  
    // Increment the margin value by 100
    height += 100;
    // Set the new margin value to the box element
    box.style.height = height + "px";
  }
});

```


or 


```javascript

// Define an object that represents the box element and its properties
var box = {
  element: document.getElementById("box"),
  width: 0,
  height: 0,
  color: "white",
  // Define a method that changes the width of the box
  changeWidth: function () {
    // Increment the width by 100
    this.width += 100;
    // Set the new width to the box element
    this.element.style.width = this.width + "px";
    // Change the background color of the box
    this.element.style.backgroundColor = "green";
    // Change the text color of the box
    this.element.style.color = "white";
  },
  // Define a method that changes the height of the box
  changeHeight: function () {
    // Increment the height by 100
    this.height += 100;
    // Set the new height to the box element
    this.element.style.height = this.height + "px";
    // Change the background color of the box
    this.element.style.backgroundColor = "green";
    // Change the text color of the box
    this.element.style.color = "white";
  }
};

// Add an event listener to the document object
document.addEventListener("keydown", function (event) {
  // Check if the right arrow key was pressed
  if (event.keyCode == 39) {
    // Call the changeWidth method of the box object
    box.changeWidth();
  }
  // Check if the left arrow key was pressed
  if (event.keyCode == 37) {
    // Call the changeHeight method of the box object
    box.changeHeight();
  }
});

```

### class Object blueprint

Creating object blueprint or template using classes.Classes work as an template for objects.
If you create a object of class the object will automatically get the older properties and methods of the class.
Means we make change on class property it will reflect to the every instance of the class (object that are created by using this class)

#### There are two ways to create class

1. class declaration : class Name{}
2. class expression : const Name=class{}

```html
<!DOCTYPE html>
<html lang="en">
<head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
          <script src="class.js" type="module"></script>
          <script src="script.js" type="module"></script>
</head>
<body>
          
</body>
</html>
```

class.js

```javascript

class Person {
          // Define a constructor method
          constructor(name, age) {
            // Assign the parameters to the properties of the object
            this.name = name;
            this.age = age;
          }
        
          // Define a method named greet
          greet() {
            // Print a greeting message using the name property
            console.log("Hello, I am " + this.name);
          }
        }
        

        export default Person;
```


script.js

```javascript
import Person from "./class.js";


        // Create a new object with the Person class
        var person1 = new Person("Alice", 25);




        // Access the properties and methods of the object
        console.log(person1.age); // 25
        person1.greet(); // Hello, I am Alice
        
```

#### Note
1. declare a class before use.
2. Place your class in separate file and import from there.



### Object Constructor function

1. There another short or less advance way for doing the same thing like a class.
2. Its "object constructor function".
3. Like class object constructor function uses a capitalized name.
4. It produces the new object by capturing the property of newly created objects.


Example1

```javascript
// constructor function
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
}

// create two objects
var person1 = new Person("Alice", "Smith", 25, "blue");
var person2 = new Person("Bob", "Jones", 30, "brown");

// access properties
console.log(person1.firstName); // Alice
console.log(person2.lastName); // Jones

```

Example2.

```javascript
// constructor function
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
  this.nationality = "English"; // add a property
  this.name = function() { // add a method
    return this.firstName + " " + this.lastName;
  };
}

// create two objects
var person1 = new Person("Alice", "Smith", 25, "blue");
var person2 = new Person("Bob", "Jones", 30, "brown");

// access properties and methods
console.log(person1.nationality); // English
console.log(person2.name()); // Bob Jones

```

#### What is the difference between class and constructor function

1. Class is a newer syntax introduced in ES2015, while constructor function is an older syntax that has been available since the beginning of JavaScript.
2. Methods are defined separately in the class but in object constructor function methods are defined with this keyword.

### Similarties

1. Both class and constructor function can be used to create multiple objects with the same properties and methods.
2. Both class and constructor function can use the new keyword to invoke them and create object instances.


```javascript
// class syntax
class Animal {
  // constructor method
  constructor(name, type, sound) {
    this.name = name; // instance property
    this.type = type; // instance property
    this.sound = sound; // instance property
  }

  // instance method
  makeSound() {
    console.log(this.name + " says " + this.sound);
  }

  // static method
  static isAnimal(obj) {
    return obj instanceof Animal;
  }
}

// create two objects using class
var dog = new Animal("Rex", "dog", "woof");
var cat = new Animal("Luna", "cat", "meow");

// access properties and methods using class
console.log(dog.name); // Rex
console.log(cat.type); // cat
dog.makeSound(); // Rex says woof
cat.makeSound(); // Luna says meow
console.log(Animal.isAnimal(dog)); // true
console.log(Animal.isAnimal(cat)); // true

// constructor function syntax
function Animal(name, type, sound) {
  this.name = name; // instance property
  this.type = type; // instance property
  this.sound = sound; // instance property

  // instance method
  this.makeSound = function() {
    console.log(this.name + " says " + this.sound);
  };
}

// static method
Animal.isAnimal = function(obj) {
  return obj instanceof Animal;
};

// create two objects using constructor function
var dog = new Animal("Rex", "dog", "woof");
var cat = new Animal("Luna", "cat", "meow");

// access properties and methods using constructor function
console.log(dog.name); // Rex
console.log(cat.type); // cat
dog.makeSound(); // Rex says woof
cat.makeSound(); // Luna says meow
console.log(Animal.isAnimal(dog)); // true
console.log(Animal.isAnimal(cat)); // true

```

### Global Objects (defined in browser)

#### Date Object 

```javascript
const rightNow = new Date();

console.log(rightNow);//Tue Oct 03 2023 11:26:08 GMT+0530 (India Standard Time)

console.log(rightNow.toDateString());//Tue Oct 03 2023
//Date is a object created with a constructor function and .toDateString() is a method defined in it?

```

### Template Literals

to inject new html in to the HTMl we need to get an element from the HTML then we are able to inject in it.
Entire document is an object in browser.

```javascript
console.log(typeof document)//object
```
When a browser renders a document it creates a document object model of that document.So that we can access DOM using Javascript.

```javascript

let a="world";

document.body.innerHtml=`hello ${a}`;
//change the body content
```
Backticks tells the browser that anything inside me is HTML or Javascript.

#### HTML expression + JS expression = Template.

Js expression is written inside dollorsign with curly brackets (${js}) .By doing this you only have to make changes in js and is reflected into HTML DOM directly.


### Before template literal 

We can also do the same thing with using simple string but it makes the things much more complicated so that Template literals comes in existance.

```javascript

let a="kumar";

document.body.innerHTML='<h1>Abhinish' + a + '</h1>';
```



# DOM

DOM stands for Document Object Model. It is a way of representing a web page as a tree of objects that can be accessed and modified by a programming language like JavaScript. For example, you can use JavaScript to change the text, color, style, or position of any element on the web page by using the DOM.

DOM describes the herarchical model in the document.

#### 1. Accessing elements with querySelector method

The queryselector and queryselectorAll both take a css query as the parameter it puts in quataition mark.

```javascript
//1 Select element main
document.querySelector('main');
//<main>…</main>


//2 Select h1 inside main
document.querySelector('main h1');
//<h1>Hello my name is abhinish kumar and i am from ludhiana</h1>


//3 Select last element of the list
document.querySelector('main ul li:last-child');
//<li>"hello 5"</li>


//4 Select all the list item (NodeList)
 document.querySelectorAll('main ul li');
//NodeList(5) [li, li, li, li, li]
```


Change the color of all the lsit 

```javascript
//1 Select all the list item and change the color of all the list item red and lst item with blue

    let nodeList = document.querySelectorAll('main ul li');

              nodeList.forEach(li=>{
                    li.style.color="red";
                              li=nodeList[nodeList.length-1];
                              li.style.color="blue"
              })

```

#### Modify element classes (single class name)

```javascript
//1 If element contain single class name(get class name)
 document.querySelector('h1').className;
//'heading'


//2 Change class name
document.querySelector('h1').className="updatedh1"
//"updatedh1"
document.querySelector('h1').className;
//"updatedh1"
```

#### Modify element classes (multiple class name)

```javascript
//1 spani has 3 classes (get all the classses)
document.querySelector('span').classList;
//DOMTokenList(3) ['first', 'second', 'third', value: 'first second third']


//2 Add new class
document.querySelector('span').classList.add("iamnew");
//undefined
document.querySelector('span').classList
//DOMTokenList(4) ['first', 'second', 'third', 'iamnew', value: 'first second third iamnew']

//3 Remove a class
document.querySelector('span').classList.remove("first");
//undefined
document.querySelector('span').classList
//DOMTokenList(2) ['second', 'third', value: 'second third']

//4 Toggle class name
 document.querySelector('span').classList.toggle("switch");
//false
    document.querySelector('span').classList.toggle("switch");
//true
    document.querySelector('span').classList.toggle("switch");
//false
    document.querySelector('span').classList.toggle("switch");
//true



// 5 Replace a class name
document.querySelector('span').classList.replace("third","newThirs");
//false
document.querySelector('span').classList
//DOMTokenList(3) ['first', 'second', 'newThirs', value: 'first second newThirs']
```

#### Handle Attributes
Anything inside a tag is called Attribute.

```javascript
//1 get all the attributes of a element
document.querySelector('img').attributes;
//NamedNodeMap {0: src, 1: alt, src: src, alt: alt, length: 2}

//2 Check element has attribute or not
document.querySelector('img').hasAttribute('src');
//true


//3 Get attribute value
document.querySelector('img').getAttribute('src');
//'img.png'


//4 Set a new attribute
document.querySelector('img').setAttribute("alt","newSet");
//undefined
document.querySelector('img')
//<img src=​"img.png" alt=​"newSet">​


//5 remove any attribute
document.querySelector("img");
//<img src=​"img.png" alt=​"newSetttttttt">​
document.querySelector("img").removeAttribute("alt");
//undefined
document.querySelector("img");
//<img src=​"img.png">​
```
You can also set the class as attribute and id ass well.

#### Inline Styling

```javascript
//1 get all styles of p
document.querySelector("p").style
//CSSStyleDeclaration {0: 'color', 1: 'background-color', accentColor: '', additiveSymbols: '', alignContent: '', alignItems: '', alignSelf: '', …}



//2 get a specific style of an element
document.querySelector("p").style.color;
//'red'



//3 Change a specific style
document.querySelector("p").style.color="blue";

```

Insted of hyphen we use camelcase for css elements

#### appending elements in DOM

```javascript
//1 Append at last
 let a=document.createElement('h1');
          a.innerHTML=`<h1>Hello</h1>`;
          
      document.querySelector("main").append(a);

//2 Append at beginning
 let a=document.createElement('h1');
          a.innerHTML=`<h1>Hello</h1>`;
          
      document.querySelector("main").prepend(a);
```

Apppend child is also common thing but it return the element.

Try it

1. replaceChild.
2. insertBefore.
3. insertAdjacentElement.


## Variables

#### Variables containers.

Being able to name things is crutial for communication.
In our code we have bunch of object.
Name is used to create a vertual container to put the object within.
In js we can put any data type to this containers.
Single equalto means the object we have on the RHS we have to put it in the container that we have on LHS.

#### Q.Why we have different type of variables?



















# 1. Array?
#### How to use and when to use.
Arrays are like a block of container we can imagine it as a train with its boxes every box is connected with its corresponding box with serial number.In javascript we can put any type of value in arrays box or container eg:number,string,boolean,object or array.
Arrays are object in javascript.

## Update array 
### How can you create an array in js

```javascript
//Arrays - Declaration
let arr = ["apple","banana","cherry"];

//Access array elements
console.log(arr[0]);  //"apple"


//It can accept any data type
let obj={name:"piyush"};
arr[3]=obj;
console.log(arr[3]);//{name:"piyush"}
console.log(arr[3].name);//"piyush"

//We can also get the length of the array
console.log(arr.length)//3

```













## a.Array Methods
Why array acctually do have methods?
Methods are functions that we call on objects with dot notation.
```javascript
arr.split();
```
here arr is object and split is a method that we call on arr object.

So over all we know that arrays are objects in javascript because of having methods.And methods are functions that are attached to all the arrays that we create.

### a-1. SLICE method
Slice method is used to extract a part from an array without changing the original array.  
Slice method is also used for strings.
```javascript
let arr=['a','b','c','d','e'];
console.log(arr.slice(2));
//Output is :-['c','d','e'];
```

here all the elements of array having index number 2 or more is split from the array(arr) and created a new array that we can see on output.

```javascript
let arr=['a','b','c','d','e'];
console.log(arr.slice(2,4));
//Output is :-['c','d'];
```
2 is starting point and 4 is the ending point to split arr.But here index 4 is not included.So that we can get the elements from index 2 to 3 only.

```javascript
let arr=['a','b','c','d','e'];
console.log(arr.slice(-2));
//Output is :-['d', 'e'];
```
-ve sign is used to get the data from the last index.
-1 is mostly used to get the last element of the array.


Q1.print all the elements of the array except first and last element.
```javascript
let arr=['a','b','c','d','e'];
console.log(arr.slice(1,-1));
//Output is :-['b', 'c', 'd'];
```

Q2.Can we create a copy of a array using slice?
yes
```javascript
let arr=['a','b','c','d','e'];
let x=arr.slice()
console.log(x);
//Output is :- ['a', 'b', 'c', 'd', 'e'];
```

or we can also copy array using spread operator
```javascript
let arr=['a','b','c','d','e'];
let x=[...arr];
console.log(x);
//Output is :- ['a', 'b', 'c', 'd', 'e'];
```

Note:you can use anyone to clone a array.

### a-2. SPLICE method

Splice is also like slice but it returns a part of the original array by mutating it.
Means we can get a part of arrary but our original array also changes while doing this.
The first parameter of splice method is similar to the slice.

```javascript
let arr=['a','b','c','d','e'];
console.log(arr.splice(2));//['c', 'd', 'e']
console.log(arr);//['a', 'b']
```

it is mostly used to delete last element of the array.Like in calculator and in add to cart functionality.

```javascript
let arr=['a','b','c','d','e'];
console.log(arr.splice(-1));//['e']
console.log(arr);//['a', 'b', 'c', 'd']
```

Second parameter is for deletecount functionality.
that deletes the number of elements that we pass in it.

```javascript
let arr=['a','b','c','d','e'];
console.log(arr.splice(1,3));//from 1st index delete next 3 elements
 //['b', 'c', 'd']
console.log(arr);//['a', 'e']
```
Third parameter is the element that we put at the place of deleted array.
Q1 Insert Apple at index 1 
```javascript
let arr=['a','b','c','d','e'];
console.log(arr.splice(1,0,"Apple");//[] 
console.log(arr);//['a', 'Apple', 'b', 'c', 'd', 'e']
```

### a-3. REVERSE method (mutates)

Used to reverse the array

```javascript
let name=['a','b','h','i','n','i','s','h'];
console.log(name.reverse());
//['h', 's', 'i', 'n', 'i', 'h', 'b', 'a']
console.log(name);
 //['h', 's', 'i', 'n', 'i', 'h', 'b', 'a']
```

```javascript
let namea='Noor';
console.log(namea.split('').reverse().join(''));
// rooN
```

### a-4. CONCAT method (non mutable)

```javascript
let a=[1,2,3,4,5];
let b=[6,7,8,9,10];
console.log(a.concat(b));
//[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
There is also another way that can concat tha arrays.

```javascript
let a=[1,2,3,4,5];
let b=[6,7,8,9,10];
console.log([...a,...b]);
//[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

### a-4. JOIN method (non mutable)


In this method we pass the separator to join the array elements with that separator.
Join method returns a new string of combined array elements.

```javascript
let a=[1,2,3,4,5];
let b=[6,7,8,9,10];
console.log([...a,...b].join('-'));
//1-2-3-4-5-6-7-8-9-10
```
It does not print the undefined and null array elements.


### a-5. new AT() method

The at() method of Array instances takes an integer value and returns the item at that index, allowing for +ve and -ve integers. Negative integers count back from the last item in the array.

```javascript
//Syntax :- at(index)
```
1. Find the element of the array at any position

```javascript
const arr=[1,2,3,4,5,6,7,8,9,10];

//with bracket notation
console.log(arr[0]);//1

//By using at()
console.log(arr.at(0));//1
```
Both work same so why we use the at() method.
The at() method is equivalent to the bracket notation when index is non-negative.
Means by using at method you can get the elements with -ve index number.

2. Find the last element of an array.
```javascript
const arr=[1,2,3,4,5,6,7,8,9,10];
//1st way
console.log(arr[arr.length-1]);//10


//2nd
console.log(arr.slice(-1));//return arr [10]
console.log(arr.slice(-1)[0]);//10


//3rd
console.log(arr.at(-1));
```
Note:-If you want to get only last element use at();
And if you want to apply chaining method to array use the method of slice and bracket notation.
3. It also works with "string"

```javascript
console.log('abhinish'.at(1));  //b
console.log('abhinish'.at(-1));  //h
```


# practice Q1
```javascript
//fins the highest bank transaction 

const tranctions=[4,34,53,75,2,6,654,75,77,3430,49];
function findha(ht){
    let re;
    for(let i=0;i<ht.length;i++){
        if(ht[i]>ht[i+1]){
            re=ht[i];
        }
    }
    return re;
}

console.log(findha(tranctions));//3430
```


### a-6. ForEach(callback) method

[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

1. ForEach is higher order function that acceps a callback function in order to what to do with the elements of the array.
2. ForEach function call the function that is passed in it by itself.
3. Callback functions are the functions that tells the higherorder functions what to do.
4. Higher order functions are the functions that acceps the another functions as an arguments and return the function as its returning value.

#### Q1. Write a functions to withdraw and deposit of monety.

```javascript
//By using for of

const movements=[200,450,-400,300,-650,-130,70,300];

for(const movement of movements){
  if(movement>0){
    console.log(`You deposit ${movement}`);
  }
  else{
    console.log(`You withdraw ${Math.abs(movement)}`);
  }
}



//Output:

You deposit 200
You deposit 450
You withdraw 400
You deposit 300
You withdraw 650
You withdraw 130
You deposit 70
You deposit 300
```


 ```javascript
//By using forEach

const movements=[200,450,-400,300,-650,-130,70,300];

movements.forEach(function(movement){
  if(movement>0){
    console.log(`You deposit ${movement}`);
  }
  else{
    console.log(`You withdraw ${Math.abs(movement)}`);
  }
})


//Output:

You deposit 200
You deposit 450
You withdraw 400
You deposit 300
You withdraw 650
You withdraw 130
You deposit 70
You deposit 300
```

How it works

1. in first iteration 0:function(200) function is called with 200.
2. in second iteration 1:function(450) function is called with 450.Tii the length of the array.

#### Q2. Write a function to withdraw and deposit of money with number of transections.

```javascript
//By using for of

const movements=[200,450,-400,300,-650,-130,70,300];

for(const [i,movement] of movements.entries()){
  if(movement>0){
    console.log(`On ${i+1} day You deposit ${movement}`);
  }
  else{
    console.log(`On ${i+1} day You withdraw ${Math.abs(movement)}`);
  }
}


//Output:

On 1 day You deposit 200
On 2 day You deposit 450
On 3 day You withdraw 400
On 4 day You deposit 300
On 5 day You withdraw 650
On 6 day You withdraw 130
On 7 day You deposit 70
On 8 day You deposit 300
```



```javascript
//By using forEach

const movements=[200,450,-400,300,-650,-130,70,300];

movements.forEach(function(movement,index,array){
  if(movement>0){
    console.log(`On ${index+1} day You deposit ${movement}`);
  }
  else{
   console.log(`On ${index+1} day You withdraw ${Math.abs(movement)}`);
  }
})

//Output:

On 1 day You deposit 200
On 2 day You deposit 450
On 3 day You withdraw 400
On 4 day You deposit 300
On 5 day You withdraw 650
On 6 day You withdraw 130
On 7 day You deposit 70
On 8 day You deposit 300
```

By using forEach its easy to do the same program.Because of the power of forEach function or method.
1. The callback function accepts (currentElement,index,fullarray).
2. Name of the parameter does not matter only matter its order.
3. Use short names (mov,i,arr).
4. Use this if you have to do the operation on array and with its index.
5. When should you use for of and wen to use the forEach.
6. You can not use continue break and continue statement.
7. SO here you use for of loop to use the break and continue to come out of the loop.

### forEach with Maps and Sets

For each is also avaliable for Maps and Sets.


### with Map()
```javascript
const currencies = new Map([
  ['key','value'],
  ['USD','United States Dollar'],
  ['EUR','Euro'],
  ['GBP','Pound Sterling']
]);


// In map the first is key and second is the value.

currencies.forEach(function(value,key,map){
  console.log(`${key}:${value}`);
})

//Output:

key:value
USD:United States Dollar
EUR:Euro
GBP:Pound Sterling
```







### with Set([iterables]) :contain uniqew value
```javascript
const currenciesUnique=new Set(['USD','GBP','USD','EUR']);
console.log(currenciesUnique);
//Set(3) { 'USD', 'GBP', 'EUR' }
```

```javascript
const currenciesUnique=new Set(['USD','GBP','USD','EUR']);

currenciesUnique.forEach(function(value,key,set){
    console.log(`${key}:${value}`);
})


//Output
USD:USD
GBP:GBP
EUR:EUR
```

The key and the value is same why is it like that.Becaue a set doesnot have keys.

This is not a misteke this is intentially dome by developers to maintain the functionallity of the forEach meth with 3 arguments.it is like (value,value,set).

or (value,_,set)._ indicates that its not necessary.


## 
[Project Bankist]("https://bankist.netlify.app/")

Dom manupulation ------18

## 1st coding chalange

1. Julie and kate are doing a study on dogs, so each of them asked five dog owners about their dogs age and store the data into an array (one array for each) For now they are just.Interested in knowing whether a dog is an adult or a puppy. A dog is an adult if it is at least three years old, and it's a puppy. If it's less than three years old.
Create a function  "checkdogs" Which asserts 2 arrays of dogs ages, ('dogsJulie' and 'dogskat').And it does the following
2. Julie found out that the owners of the first and the last Two dogs actually have cats, not dogs. So creators shallow copy of Julies array and.Remove the cat edges from the.Copied array (because it's a bad practice to mutate function parameters).
3.  Create an array with both  julies, corrected and kathe data.
4.  for each remaining dog load to the console where it's an adult ("dog One is an adult and is five years old') or a puppy ('Dog number 2 is still a puppy')
5.  Run the funciton for both test database.

```javascript

```


# String manipulation (master)

#### 1. Q Find the length of the password.

Ans :-Js has a built in length property length.It returns the string as a number.

```javascript
const success="Success";
const needLongPassword="Password should be atleast 8 charachters";

function findPassLength(password){
    return password.length>=8?success:needLongPassword;
}

console.log(findPassLength("1234567"))
console.log(findPassLength("12345676744"))


\\ Password should be atleast 8 charachters
\\ Success
```

#### 2. Trim the empty spaces at the beginning and end of the string.(save password with no side white space).

Ans 
```javascript
const success="Success";
const needLongPassword="Password should be atleast 8 charachters";

function findPassLength(password){
    console.log("before trim "+ password.length)
    console.log("afterr trim" + password.trim().length)
    
}

findPassLength("  1234567  ")
findPassLength("  12345676744  ")

\\before trim 11
\\afterr trim7
\\before trim 15
\\afterr trim11
```

#### 3. Chech the phone number and check its country code.(string.startsWith()).

Ans string.startsWith()

a. Returns a boolean (true or false) based on whether the search string is found.
b. startsWith() has two parameters : the search string that we are looking for and the position where we want to start the search.

```javascript
const success="valid";
const unvalid="Unvalid phone number";

function findPassLength(number){
    return number.startsWith("+91")?success:unvalid;
    
}

console.log(findPassLength("+9188728198"))
console.log(findPassLength("+82827328"))
console.log(findPassLength("91827328"))

\\valid
\\Unvalid phone number
\\Unvalid phone number

```
#### 4. return the city string in all lowercase letters.
Ans: string.toLowerCase()

a. Return a new string in all lowercse letters
 --Does not modify the original string.
b toLowerCase() does not taking any arguments.

```javascript
function findPassLength(a="This Is my citY"){
    return a.toLowerCase();
    
}

console.log(findPassLength())

\\this is my city

```


#### 5. Return the heading in all uppercase letters.
Ans: string.toUpperCase().

a. Return a new string in all uppercase letters
--Does not modify the original string
b. toUpperCase() does not take any arguments.

```javascript
function findPassLength(a="This Is my citY"){
    return a.toUpperCase();
    
}

console.log(findPassLength())

\\this is my city

```

#### 6. Determine if the word "fun" is included in a string.
Ans: string.includes()

a. Return a boolean based on whether or not the search string was found.
b. includes() takes one required arguments, which is the string that is going to be searched for in the string the method is applied to.

```javascript
const positive="positive";
const negative="negative";

function hasFun(message){
    return message.includes("fun")?positive.toUpperCase():negative.toUpperCase();
    
}

console.log(hasFun("this is a funny video"))
console.log(hasFun("this is a bad video"))

\\POSITIVE
\\NEGATIVE
```

#### 7. Return an array with email based on the striing provided.
Ans: string.split();

a. Returns an array of strings based on the separator 
b. split() takes two arguments.
--Separator-lets the method knows where you want to divide up the string.
--Limit(optional) - specifies if you want to limit the number of entries in the array.

```javascript

function splitEmil(emailList){
    return emailList.split(", ");
}

console.log(splitEmil("apple.@gmail.com,ball.@gmail.com,cat.@gmail.com"))

\\[ 'apple.@gmail.com,ball.@gmail.com,cat.@gmail.com' ]
```

#### 8. Return a slice string with the last four digits of an account number.
Ans: string.slice()
a. Return an extracted section of a string.
--Does not modify the original string.
b. slice() has two parameters:
--indexStart(required)-index of the first character to include in the returned substring.

--indexEnd(optional)--index of the first character to exclude from the returned substring.

```javascript
function getLastNumner(accNumber){
    return accNumber.slice(5);
}

console.log(getLastNumner("123456789"))

\\6789

```


#### 9. Update the typo in the string of emails.

Ans string.replace()

a. Returns a new string with the all the instances matched by the replacement text.
--Does not modify the original string.
b. replace() has two parameters: the pattern that needs to be replaced and the actual replacement.

```javascript
function splitEmil(emailList){
    return emailList.replace('gmail.com','npm.com')
}

console.log(splitEmil("apple.@gmail.com,ball.@gmail.com,cat.@gmail.com"))

\\apple.@npm.com,ball.@gmail.com,cat.@gmail.com

```

#### 10. Combine two strings into a single string.
Ans: string.concat();
a. Return a new ,concatenated string
--Does not modify the original string
b. concat() can take as many parameters/strings as needed depending on what is going to be concatenated.

```javascript
function splitEmil(fname="abhi",lname="kumar",other="Big b"){
    return fname.concat(" ",lname," ",other);
}

console.log(splitEmil())
```




# Asynchronous Javascript

Tim Berners-Lee is the inventor of the World Wide Web, which is a system of interlinked hypertext documents that can be accessed via the Internet. He created the first web browser, web server, HTML, URL, and HTTP in the late 1980s and early 1990s while working at CERN, a European research organization. He also founded and directed the World Wide Web Consortium (W3C), which oversees the standards and development of the Web. He is a professor at the University of Oxford and MIT, and a recipient of many awards and honors for his invention1


1. Sir Tim Berners-Lee invented the WWW in 1989.

2. All the internet is just a web of wires and wires has no any knowledge where to transfer the data.
3. So we need a protocol ,Its like a standard that every one follows.
4. HTTP is a protocol that allows the fetching of resources such as HTML document(thats why it is called as hypertext transfer protocol)
5. By the ombination of http and html we have www.
6. HTTP are the protocols or the rules that we use over the wire.
7. HTTP is the foundation of any data exchange on the web.
8. HTTP is a common language that a client and a server use to communicate.(we say to server can you give me this file server responses with that file).Because thy both understand their languanges.
9. The message send by the browser is called as request and the messages send by the server is called as response.

#### HTTP 

This language has only little words to communicate with the server 

1. GET:used to get the file from the server.
2. POST:you post something in the server.
3. PUT:used to ipdate the data on the server.
4. Delete:used to delete a piece of data on the server.

example like in twitter get is used to get the twitter feed ,post is used to post your data or new user id to the server.put is used used to edit your tweet.Delete is used to delete your user account or a tweet.

Http is also used to get the video,audio and ajax to update our html page.

#### HTTP messages

1. 200 :successful.
2. 400 :not found.
3. 500 : server error.

your http request goes to the server and ask to the server to give you required file and if file not exist it will show you the http status 440 not found.

## GET 

```html
<form method="GET">
<register>Register now</register>
</form>
```

Open the netword tool in devtoolbar.
If you click the resiger button it will modify the link (?ada?adsa?adsasd?Adas) this is called a query string .it is the first way of sending the data to the server.
The query string contains the (key value pair).

##### its not secure your passord is open for every one.(send the data through header)

The second way of sending the data to server is through body.

## POST request

```html
<form method="POST">
<register>Register now</register>
</form>
```

It does not create a query string on the link.
It store the form data.

### The password was visible on both the cases ?

Think a person watching our communication it will get our password from query string.
And if we send the data through body 
The hacker find the way to get your request to him first.See your password in the body of the form.


## Use HTTPS to secure your data from hackers..

HTTPS means hypertext transfer protocol secure.The communication from server to browser is now encrypted.It means that only server and client has the key to open or to read this message.


The s in https uses a layer called transport security layer(secure socket layer) TSL and SSl for short.
By using https even a third person get the request but he does not read this Because the password is now not in redable form.

## NOTE when you are login into the account chect the https first.

Summary ,Your browser is a http client sending a request to the server machine.
When a client clicks to a hyper link the browser builts an http request and sends it to the server to communicate now the server gives us the data as a response.



# JSON

We can not send any type of data to server to communicate ,it can only be text.
We cant not send a javascript object.
JS object is very confusing for the errver because the server can be written in to java,php or in other language but string is understandable for every languages.

1. JSON stands for javascript object notation.
2. JSON is a syntax for storing and exchanging data.
3. JSON is text,written with javascript object notation.


THERe is also another form XML.
Both XML and JSON use to transfer the data over  the server.

JSON uses object like syntax.and XML uses html like syntax.

1. To send the data to the server we have to sonver our data in to JSON formet.and the server changes it to their own language to understand.
2. And server then changes the request data to the JSON and send back to you.
3. And to read the responsive you have to change the formed again.

## JSON in javascript

Javascript comes with its own json functions to deal with json formet.

```javascript
//json to object
//1. JSON.parse() 

var obj=JSON.parse('{"name":"john","age":30}');

//object to json
//2. JSON.stringify()

var myJSON = JSON.stringify(obj);

```

JSON is text and we can conver any javascript object to json and send json to the server.we can also conver any type of json data of server into a object.



# AJAX 

Onevery time we make a request our page refresh ever for json request.

If you want to request any thing your whole page reload on every request.
It causes a poor user experience.

We have AJAX that loads the data without disturbing the other part of your web page or without reloding.


#### what is AJAX 
Its a technology to combine pieces together,Its calles xml http request.

1. it was very complecated before.
2. its complexicity was handled by jquery thats why jquery was very famus.
3. Now we have a FETCH in javascript for ajax call.

```javascript
fetch('/my/url').then(response=>{
console.log(response);
});

```

fetch does http for us.


Summry,when a event occur on a web page to login we send our detail to server and server responses that you are loged in and all these happen without refreshing the page with AJAX ,ajax is used to create a single page application.In SPA our page holds only required data and if we request to the new data AJAX vanish the previous data and rebuild that part with new data.


#### example

```javascript
//fetch is a window object
//fetch is a api
fetch('https://jsonplaceholder.typicode.com/users')
.then(response=>response.json())
.then(user=>console.log(user));
```


```javascript
//console
fetch('https://jsonplaceholder.typicode.com/users')
//promise
fetch('https://jsonplaceholder.typicode.com/users')
.then(response=>console.log(response));
//fullfill
```
Fetch comes with their own .json() method to convert response formet.


# Promises (ES6)
Promises are new features in javascript.

#### Q1.What is a Promise in JavaScript?
Ans:- A promise is an object that may produce a single value some time in the future.
Either a resolved value or a reason that its not resolved(rejected).

more:::A promise is a way of handling asynchronous operations in JavaScript, which means operations that take some time to complete and may not have a fixed outcome. For example, you can use a promise to request some data from a server, and then do something with the data when it arrives.

#### Q2.What are the states of a Promise?
Ans:-A Promise can be in one of three states: pending, fulfilled, or rejected.

#### Q3.How do you create a Promise in JavaScript?
Ans:-You can create a Promise using the Promise constructor, which takes a single function (known as the executor function) and it defines what the promise will do and how it will resolve or reject. 

more::::The executor function has two parameters: resolve and reject. These are also functions that you can call inside the executor function to indicate the outcome of the promise. If the promise is successful, you call resolve with the value that you want to return from the promise. If the promise fails, you call reject with the reason for the failure.


```javascript
//Promise constructor
// create a new promise
let coinToss = new Promise(function(resolve, reject) {
  // simulate a coin toss with a random number
  let randomNumber = Math.random();
  // if the number is greater than 0.5, resolve with "Heads"
  if (randomNumber > 0.5) {
    resolve("Heads");
  }
  // otherwise, reject with "Tails"
  else {
    reject("Tails");
  }
});

```

##### Explain the code 
In this example, we create a new promise called coinToss that uses the Promise constructor with an executor function. Inside the executor function, we generate a random number between 0 and 1 using Math.random(). If the number is greater than 0.5, we call resolve with the value “Heads”. Otherwise, we call reject with the value “Tails”.
This promise will either resolve with “Heads” or reject with “Tails” depending on the random number. To use the value or the reason of the promise, we need to attach handlers to it using the .then() and .catch() methods. For example:

```javascript
// use the coinToss promise
coinToss
  // attach a handler for success
  .then(function(value) {
    // log the value of the promise
    console.log("The coin landed on " + value);
  })
  // attach a handler for failure
  .catch(function(reason) {
    // log the reason of the promise
    console.log("The coin landed on " + reason);
  });

```

##### Explain the code 
In this example, we use the coinToss promise and attach two handlers to it using .then() and .catch(). The .then() method takes a function that will be called if the promise resolves, and receives the value of the promise as an argument. The .catch() method takes a function that will be called if the promise rejects, and receives the reason of the promise as an argument.

The output of this code will be either “The coin landed on Heads” or “The coin landed on Tails” depending on the random number.

#### Q4.How do you handle the result of a Promise?
Ans:-You can use the .then() method to handle the successful resolution of a Promise and the .catch() method to handle any errors that occur.

#### Q5.How do you chain multiple Promises together?
You can chain Promises together using the .then() method, which returns a new Promise that resolves to the value returned by the callback function.
###### more
To chain multiple promises together, you can use the .then() method of the promise object. The .then() method takes a function as an argument, which will be called when the promise is resolved. The function can return another promise, which will be passed to the next .then() method in the chain. This way, you can perform multiple asynchronous operations in a sequence, where the output of one operation is used as the input for the next operation.

For example, suppose you want to fetch some data from a server, and then use that data to fetch some more data from another server. You can use promise chaining to do that:

```javascript
// create a promise to fetch data from server A
let promiseA = fetch('https://serverA.com/data.json');

// chain a .then() method to handle the response
promiseA.then(function(response) {
  // convert the response to JSON and return another promise
  return response.json();
})
// chain another .then() method to handle the JSON data
.then(function(data) {
  // use the data to fetch data from server B and return another promise
  return fetch('https://serverB.com/data/' + data.id);
})
// chain another .then() method to handle the response from server B
.then(function(response) {
  // convert the response to JSON and return another promise
  return response.json();
})
// chain another .then() method to handle the JSON data from server B
.then(function(data) {
  // use the data to do something else
  console.log(data);
});

```
##### Explain code 
n this example, we create a promise to fetch data from server A, and then chain four .then() methods to handle the responses and data. Each .then() method returns another promise, which is passed to the next .then() method in the chain. The final .then() method uses the data from server B to do something else.

This way, we can perform multiple asynchronous operations in a sequence, using promise chaining. 


#### Q6.How do you handle errors in a Promise chain?
Ans:-You can use the .catch() method to handle errors that occur in a Promise chain.But it can catch the error only in the code that defines before it.In promise chaining.

###### more 
A Promise chain is a sequence of asynchronous operations that are linked by the .then() method. Each .then() method takes a function that receives the result of the previous operation and returns a new Promise. This way, you can perform multiple tasks one after another, using the output of one task as the input for the next one.

For example, suppose you want to fetch some data from a server, parse it as JSON, and then display it on the web page. You can use a Promise chain like this:
```javascript
fetch('/data.json') // returns a Promise that resolves to a Response object
  .then(response => response.json()) // returns a Promise that resolves to the parsed JSON data
  .then(data => {
    // do something with the data, such as displaying it on the web page
    console.log(data);
  });

```
However, sometimes things can go wrong in a Promise chain. For example, the server might be down, or the data might be invalid. In that case, you need to handle the errors gracefully and avoid crashing your program.

To handle any errors that may occur in the chain, you can add a call to .catch() at the end of the chain. If any of the Promises are rejected, this catch handler will run, and the rest of the chain is skipped1.

For example, suppose you want to handle any errors that might happen in the previous example. You can add a .catch() method like this:

```javascript
fetch('/data.json') // returns a Promise that resolves to a Response object
  .then(response => response.json()) // returns a Promise that resolves to the parsed JSON data
  .then(data => {
    // do something with the data, such as displaying it on the web page
    console.log(data);
  })
  .catch(error => {
    // handle any errors that might occur in the chain
    console.error(error);
    alert('Something went wrong!');
  });

```

This way, if any of the Promises in the chain are rejected, the catch handler will run and display an error message to the user.

You can also handle errors at any point in the chain by adding a second argument to the .then() method. This argument is a function that receives the error from the previous operation and returns a new Promise. This way, you can recover from some errors and continue with the chain2.

#### Q7.What is the difference between Promise.resolve() and Promise.reject()?
Promise.resolve() returns a Promise that is already resolved with a value, while Promise.reject() returns a Promise that is already rejected with an error.

```javascript
// A promise that is resolved with the value 42 let promiseA = Promise.resolve(42);

// A promise that is rejected with the error “Something went wrong” let promiseB = Promise.reject(new Error(“Something went wrong”));
```

#### Q8.What is the purpose of the Promise.all() method?
The Promise.all() method takes an array of Promises and returns a new Promise that resolves when all of the input Promises have resolved.

```javascript
// Create three promises that resolve after different delays let promise1 = new Promise((resolve, reject) => { setTimeout(() => { resolve(“First”); }, 1000); });

let promise2 = new Promise((resolve, reject) => { setTimeout(() => { resolve(“Second”); }, 2000); });

let promise3 = new Promise((resolve, reject) => { setTimeout(() => { resolve(“Third”); }, 3000); });

// Use Promise.all() to wait for all of them to finish Promise.all([promise1, promise2, promise3]).then((values) => { // This will run after all promises resolve console.log(values); // [“First”, “Second”, “Third”] }).catch((error) => { // This will run if any promise rejects console.error(error); });
```

```javascript
let urls=[
    "https://jsonplaceholder.typicode.com/users",
    "https://jsonplaceholder.typicode.com/photos",
    "https://jsonplaceholder.typicode.com/albums"    ];
    
   Promise.all(urls.map(url=>{
    return fetch(url).then(resp=>resp.json())
})).then(result=>{
    console.log(result[0]);
    console.log(result[1]);
    console.log(result[2]);
}) // Add this parenthesis
```

[More](https://testbook.com/interview/javascript-promise-interview-questions)


# Fetch api 
fetch api is a build in tool in browser used to fetch the data asynchronously from different netwirk requiest by using GET<POST<PUT 
fetch api contain first argument a http link and second argument is type of request.


```javascript

console.log(fetch('https://reqres.in/api/users'));

>>>Promise{pending}
```

Fetch is a promise based api 



```javascript

console.log(fetch('https://reqres.in/api/users'));
.then(res => console.log(res));

>>>>Response{data object}
```
We are not able to access the body of returned data by using Response,we have to convert it into JSON formet.

```javascript

console.log(fetch('https://reqres.in/api/users/1'));
.then(res =>res.json())
.then(data => console.log(data));

>>>>{data object}
```

fetch will alwas succeed so to detect the uncessful we use


```javascript

fetch('https://reqres.in/api/users/1')
.then(res =>{

if(res.ok){
console.log("SUccess");
}else{
console.log("Not Successful")
}
res.json()

})
.then(data => console.log(data));

>>>>{data object}
```

Fetch is used to do some more operations with data,it can post the data delete the data from server and do a lot of things.












