### Problem 
- Give a number 'n', find the nth element of the Fibonacci sequence
In mathematics, the Fibonacci sequence is a sequence in which each number is the sum of the two preceding ones..
- The first two numbers in the sequence are 0 and 1. (0, 1, 1, 2, 3, 5, 8...)
- recursive Fibonacci(0) = 0
- recursive Fibonacci(1) = 1
- recursive Fibonacci(6) = 8

﻿

### Tips for recursive solutions
_______________
- Figure out how to break down the problem into smaller versions of the same problem
- Identify the base case for recursion


```js
function recursiveFibonacci(n){
   if(n<2){
      return n ;
   }
   return recursiveFibonacci(n-1)  + recursiveFibonacci(n-2)
}
//big-o  O(2^n)
```


```scss
recursiveFibonacci(6)
   |
   └── recursiveFibonacci(5)
          |
          ├── recursiveFibonacci(4)
          |       |
          |       ├── recursiveFibonacci(3)
          |       |       |
          |       |       ├── recursiveFibonacci(2)
          |       |       |       |
          |       |       |       ├── recursiveFibonacci(1) -> 1
          |       |       |       └── recursiveFibonacci(0) -> 0
          |       |       └── recursiveFibonacci(1) -> 1
          |       |
          |       └── recursiveFibonacci(2) -> 1
          |
          └── recursiveFibonacci(4)
                 |
                 ├── recursiveFibonacci(3) -> 2
                 └── recursiveFibonacci(2) -> 1

```


mycode 

```js
function fibonacci (n,arr = [0,1]){
    let len  = arr.length 
    if(len === n )return arr
    arr.push(arr[len-1] + arr[len-2])
     return fibonacci(n,arr)
}
console.log(fibonacci(6)) //[ 0, 1, 1, 2, 3, 5 ]
```