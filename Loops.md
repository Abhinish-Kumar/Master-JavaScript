# Loops in Javascript

## While Loop 

```javascript

while(consition){

//Looop Body , code here to repeat

}

```

As long as the condition is true the code inside loop body keep running. 

```javascript

let i = 0;
while(i<3){

//print 0 then 1 then 2
//start from 0 till one less then 3
console.log(i);
i++; //update loop each time

}

```

Condition in while loop can be anything , not only the comparison. It may be any true value. 

```javascript

while(i!=0) ===== while(i)

//both are same
```


```javascript

let i = 3;
while(i){
//run till it has number more then 0
//0 is a falsy value
//print 3 then 2, then 1
console.log(i);
i--;
}

```

Loop will run as long as i is not 0. 

Note:- If you have only one line to repeat then you can skip the {} curly braces.


```javascript

let i = 3;
while(i) console.log(i--);

//3, 2 ,1

let i = 3;
while(i)
console.log(i--)

//3, 2 ,1

```


## do-while

It runs the loop first then it checks that it should repeat that or not. 
You can check the condtion after the loop body executed.

```javascript

do{
//loop body, write your code here
}while(condition)

```

```javascript

let i = 0;
do{
console.log(i);
i++
}while(i<3);


//Output:

//0
//1
//2

```
This type of loop you use when you want to run the loop body , at least once, no matter condition is true or false.





















