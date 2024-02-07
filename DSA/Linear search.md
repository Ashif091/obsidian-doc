
### Problem
- Given an array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.
   - `arr =  [-5, 2, 10, 4, 6], t = 10 -> Should return 2`
   - `arr = [-5, 2, 10, 4, 6], t = 6 -> Should return 4`
   - `arr = [-5, 2, 10, 4, 6], t = 20 -> Should return -1`

#### My Approach

```js
function linearSearch (arr,n){
   for(let i = 0 ; i < arr.length ; i++){
      if(arr[i]===n ){
         return i
      }
   }
   return -1;
}
// BIG-O NOTATION O(n) 
```

### Master Approach  

```js
same
// BIG-O NOTATION O(n) 
```






1-04