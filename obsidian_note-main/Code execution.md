![[Pasted image 20230807105942.png|325]]

### JAVASCRIPT is a synchronous single-threaded language 
```js
const n = 2;
function double(n){ //a parameter get here
    let rst = n*2;
    return rst;
}                 //argument pass here  
let ans = double(n); //(funtion invocation ) if this run a brandnew execution is created
```

##### The global execution context

memory  allocation |  code execution
-------------------|------------------
const = default  |     
double{......}|    when we call the faction it will create other memory allocation
ans = default |

#### A exple 
![[Pasted image 20230807130803.png|450]]
#### call stack memory 
1. When the program starts, the global context is added to the call stack.
    
2. Whenever a function is called, its context (including variables and arguments) is added to the top of the call stack.
    
3. The function at the top of the call stack is the one currently being executed.
    
4. When a function completes its execution, its context is removed from the top of the call stack, and the control returns to the function that was below it.
    
5. This process continues until all functions have been executed, and the call stack becomes empty again.

 *After the all execution, the call stack memory will clear* 


 #Undefined 
 ## undefined 
 [YouTube link](https://www.youtube.com/watch?v=B7iF6G3EyIk&list=PLlasXeu85E9cQ32gLCvAvr9vNaUccPVNP&index=7)
 undefined is keyword which is =to variable 
 ```js 
 var a ;
 console.log(a===undefined); //it is true 
```
 - in stack memory which is store like a key word 
 - undefined and not defined is entirely 
		 
 1) **Undefined:** "Undefined" is a special value in JavaScript that indicates the absence of a value. It is a primitive data type. When a variable is declared but not assigned a value, its default value is `undefined`.
 ```js
 let x; // x is declared but not assigned a value, so it's undefined
console.log(x); // Outputs: undefined

```
 2) **Not Defined:** "Not defined" refers to a situation where a variable or identifier is used without being declared anywhere in the scope. This will result in a `ReferenceError`, indicating that the identifier is not recognized.
  ```js
  console.log(y); // Results in a ReferenceError: y is not defined

```





page id =  293734