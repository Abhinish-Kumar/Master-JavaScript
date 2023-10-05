# Master-JavaScript (advance level)
[
<img src="https://abhinish-kumar.github.io/Portfolio./logo.jpg" width="200px">](https://abhinish-kumar.github.io/Portfolio./)
This is a master course of JavaScript. In this course you can learn how the things works in JavaScript when to use and how to use it. All the topics are in readme format.

## Story of JavaScript 
<img src="https://th.bing.com/th/id/OIP.DpeuhHbnB6m2uE2A5UTpBAHaFj?w=240&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7" width="200px">
Brendan Eich: -The developer of JavaScript.


In 1993, the first web-browser was released, named Mosaic. After which Netscape Corporation was established and Netscape Navigator was released in 1994. In 1995, Netscape decided to add a scripting language to the Navigator, and Brendan Eich was hired to develop it. In 10 days, JavaScript was ready and named Live Script. In December 1995, it was renamed from Live Script to JavaScript. There was also a big reason behind naming JavaScript because at that time Java language was very famous, so they named JavaScript similar to Java to get fame in the market.

<img src="https://www.versionmuseum.com/images/applications/netscape-browser/netscape-browser%5E1995%5Enetscape-navigator-2.0-mac.jpg" width="200px">
Netscape Navigator(web-browser)

After this, Microsoft introduced its own web browser in 1995, which was named Internet Explorer. Now due to two web-browsers in the market, the browser war between Netscape Navigator and Internet Explorer has started. Microsoft created a new language for its Internet Explorer called JScript by reverse engineering. JScript was first released in 1996, which supported CSS. The biggest problem with this was that the web developer had to connect with more users, for which he had to work separately for both browsers. Later, Internet Explorer covered 95% of the market at the cost of its brand.

<img src="https://media.dcnews.ro/image/202105/w1200/logo-internet-explorer_66183000.jpg" width="200px">
Internet Explorer(browser)

Now it's time for the third browser. The third browser was released in 2004 by Mozilla called Firefox.


<img src="https://th.bing.com/th/id/OIP.met2AGps8yR80QgnYwdvgAHaHe?pid=ImgDet&rs=1" width="200px">
Firefox(browser)

Everyone was releasing their own web browser, so Google was also going to lag behind. Google released its browser, named Google chrome in 2008.it was the most powerful browser ever used the V8 engine in it.

<img src="https://th.bing.com/th/id/OIP.eWgDcQjWpovhVepWuer9jgHaD5?pid=ImgDet&rs=1" width="200px">
Google Chrome(browser)

For so many browsers, the web developer had to write code that would support all browsers. This work took a lot of time and was also a bit confusing. To solve this problem, a conference was held in 2008 and an agreement was reached with all browser companies that all would use the same standard language for their browsers. Script 5 was then standardized in December 2009, which was supported in all browsers. The biggest update for JavaScript was ECMAScript 6, which added a lot of new features in it like let const  arrow function etc.


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













# 1. Array?
#### How to use and when to use.
Arrays are like a block of container we can imagine it as a train with its boxes every box is connected with its corresponding box with serial number.In javascript we can put any type of value in arrays box or container eg:number,string,boolean,object or array.
Arrays are object in javascript.
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








