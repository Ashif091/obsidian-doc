### Problem 
- Given an array of integers, sort the array.
   - `const arr = [-6, 20, 8, -2, 4]`
   - `MergeSort(arr) => Should return [-6, -2, 4, 8, 20]`
  ﻿

### Insertion sort idea
- Divide the array into sub arrays, each containing only one element (An array with one element is considered sorted)
- Repeatedly merge the sub arrays to produce new sorted sub arrays until there is only one sub array remaining. That will be the sorted array.


![[Pasted image 20240207112416.png]]![[Pasted image 20240207112421.png]]

### Master Approach  

```js
function MergeSort(arr) {
   if(arr.length <2){
      return arr
   }
   let middleIndex = Math.floor(arr.length/2)
   let leftArr =arr.slice(0,middleIndex)
   let rightArr = arr.slice(middleIndex)
   
   return merge(MergeSort(leftArr),MergeSort(rightArr))
}

  

function merge(leftArr , rightArr) {
   let sortedArr = []
   
   while (leftArr.length & rightArr.length){
      if(leftArr[0]<rightArr[0]){
         sortedArr.push(leftArr.shift())
      }else{
         sortedArr.push(rightArr.shift())
      }
   }
   return [...sortedArr,...leftArr,...rightArr]
}
//big-O O(nlogn)
```

