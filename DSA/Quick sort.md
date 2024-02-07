### Problem 
- Given an array of integers, sort the array.
   - `const arr = [-6, 20, 8, -2, 4]`
   - `QuickSort(arr) => Should return [-6, -2, 4, 8, 20]`
  ﻿

### Insertion sort idea
- Identify the pivot element in the array ﻿
	- Pick first element as pivot
	- Pick last element as pivot (Our approach)
	- Pick a random element as pivot
	- Pick median as pivot
- Put everything that's smaller than the pivot into a 'left' array and everything that's greater than the pivot into a 'right' array
- Repeat the process for the individual 'left' and 'right' arrays till you have an array of length 1 which is sorted by definition
- Repeatedly concatenate the left array, pivot and right array till one sorted array remains

![[Pasted image 20240207094823.png]]

### Master Approach  

```js
function QuickSort(arr) {
   if(arr.length < 2){
      return arr
   }
   let pivet = arr[arr.length - 1];
   let left = [];
   let right = [];
   
   for (let i = 0; i < arr.length - 1; i++) {
      if(arr[i] < pivet){
         left.push(arr[i])
      }else{
         right.push(arr[i])
      }
   }
   return [...QuickSort(left),pivet,...QuickSort(right)]
}
// wost case O(n^2)
//avarage case O(nlogn)
```

