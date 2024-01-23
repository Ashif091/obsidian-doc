- <span style="color:#00b0f0">The curried function returns a new function for each argument it expects. </span>
- When you call these generated functions with the required arguments one by one, you eventually get the result of the original function.
____________________

```js
//in normal methord
function sum  ( a,b) {
    return a+b;
}
console.log(sum(3,5))  

//with Currying
function x(a){
    return(function(b){
      return a+b;
   })
}
let a1=x(5)
  console.log(a1(3))
```

--------------------------


```js
// Regular function that takes two arguments
function add(a, b) {
  return a + b;
}

// Curried version of the add function
function curriedAdd(a) {
  return function(b) {
    return a + b;
  };
}

// Using the curried function
const add5 = curriedAdd(5);
console.log(add5(3)); // Outputs: 8

```






























12*