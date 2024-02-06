### Problem
- Give a positive integer 'n', determine if the number is a power of 2 or not An integer is a power of two if there exists an integer 'x' such that 'n' === 2x.
   - `isPowerOfTwo(1) = true (2^0)`
   - `isPowerOfTwo(2) = true (2^1)`
   - `isPowerOfTwo(8) = true (2^3)`
   

#### My Approach

```js
function isPowerTwo(n) {
   let value = 1
   let i ;
   for (i = 0; n > value; i++) {
      value = value * 2
   }
   if(n<value){
      return false
   }
   return true ;
}
// BIG-O NOTATION O() 
```

### Master Approach  

```js
function isPowerTwo(n) {
   if(n<1){
      return false ;
   }
   while (n>1) {
      if(n%2!==0){
         return false
      }
      n = n/2
   }
   return true ;
}
// BIG-O NOTATION O(logn) 
```

#### Big-O constant 

```js
function isPowerTwoBitWise & (n) {
   if(n<1){
      return false ;
   }
   return (n & (n-1))===0;
}
// BIG-O NOTATION O(1) 
```



1-03