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

1. Q Find the length of the password.

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

2. Trim the empty spaces at the beginning and end of the string.(save password with no side white space).

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

3. Chech the phone number and check its country code.(string.startsWith()).

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






















