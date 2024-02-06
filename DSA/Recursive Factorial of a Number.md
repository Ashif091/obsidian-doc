### Problem 
- Give an integer 'n', find the factorial of that integer
The factorial of a non-negative integer 'n', denoted n!, is the product of all positive integers less than or equal to 'n'.
- `Factorial of zero is 1.`
- `factorial(4) = 4*3*2*1= 24`
- `factorial(5) = 5*4*3*2*1 = 120`

﻿

### Tips for recursive solutions
_______________
- Figure out how to break down the problem into smaller versions of the same problem
- Identify the base case for recursion


```js
function recursivefactorial(n){
   if(n<2){
      return 1 ;
   }
   return n * recursivefactorial(n-1)
}
//big-o  O(n) linear 
``` 


```js
recursivefactorial(4)
   |
   └── recursivefactorial(3)
          |
          ├── recursivefactorial(2)
          |       |
          |       ├── recursivefactorial(1)
          |       |       |
          |       |       └── recursivefactorial(0)
          |       |               |
          |       |               └── return 1
          |       |
          |       └── return 2 * 1 = 2
          |
          └── return 3 * 2 = 6


```

