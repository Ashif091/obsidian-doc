### Problem 
- Give an integer 'n', find the factorial of that integerIn mathematics, the factorial of a non-negative integer 'n', denoted n!, is the product of all positive integers less than or equal to 'n'.
   - `Factorial of zero is 1`
   - `factorial (4) = 4*3*2*1 = 24`
   - `factorial(5) = 5*4*3*2*1 = 120`

#### My Approach

```js
function factorial (n){
   let result = 1;
   for(let i = n  ;  i > 1 ; i--){
      result = result * i
   }
   return result ;
}
// BIG-O NOTATION O[N]
```

### Master Approach  

```js
function factorial (n){
   let result = 1;
   for(let i = 2  ;  i <= n ; i++){
      result = result * i
   }
   return result ;
}
// BIG-O NOTATION O[N] (linear)
```




1-03