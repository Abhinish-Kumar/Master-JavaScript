# Master-JavaScript (advance level)
<img src="https://abhinish-kumar.github.io/Portfolio./logo.jpg" width="200px">
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






