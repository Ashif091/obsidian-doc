### Problem 
- Give a natural number 'n', determine if the number is prime or not. A prime number is a natural number greater than 1 that is not a product of two smaller natural numbers.
   - `isPrime(5) = true (1*5 or 5*1)`
   - `isPrime(4) = false ( 1*4 or 2*2 or 4*1)`
   

#### My Approach

```js
function isPrime (n){
 let result = true ;
 n===1||n===undefined?result=false:'';
 for(let i = 2 ;i<=n/2 ;i++){
   if(n%i===0){
      result=false;
      break ;
   }  
 }
 return result;
}
// BIG-O NOTATION O(n/2) 
```

### Master Approach  

```js
function isPrime (n){
 if(n<2){
   return false ;
 }
 for( let i=2 ; i<=Math.sqrt(n) ; i++){
   if(n%i===0){
      return false ;
   }
 }
 return true;
}
// BIG-O NOTATION O(sqrt(n)) 
```




1-03