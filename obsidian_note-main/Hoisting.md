#### In JavaScript, a variable can be declared after it has been used.
In other words; a variable can be used before it has been declared([[Code execution]]).

```js
var pkr = "pkr is working"
function srk(){
    console.log('hi this is working very well ');
}

srk();
console.log(pkr)
```
out put :
hi this is working very well
pkr is working

```js
srk(); //function indepent on the hoisting 
console.log(pkr)
var pkr = "pkr is working" 

function srk(){
    console.log('hi this is working very well ');
}

```
 out put :
 hi this is working very well
 undefined
 -------------------------
 ##### here if u use #let #const ([[let_and_const]]) in the case of function  then out put is like;
 ```js
 ReferenceError ❌
```
##### if u use  #arrowfuntion  it will undefined 
```js
console.log(rpm);
 var  rpm = () => {

    console.log('hi hello ')
}
```
it is due to it will save in global memory as variable 

##### if u assign a function to a var
  it will save as a variable in global memory 
  ```js
  console.log(fun)
var fun = function srk(){
console.log('HI')
}
---out---
undefined
``` 

 
 
 
 
 
 
 
 12*