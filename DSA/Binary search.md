### Problem
- Given a sorted array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.
   - `arr =  [-5, 2, 4, 6, 10], t = 10 -> Should return 2`
   - `arr = [-5, 2, 4, 6, 10], t = 6 -> Should return 4`
   - `arr = [-5, 2, 4, 6, 10], t = 20 -> Should return -1`
### Binary search pseudocode
- If the array is empty, return -1 as the element cannot be found.
- If the array has elements, find the middle element in the array. If target is equal to the middle element, return the middle element index.
- If target is less than the middle element, binary search left half of the array.
- If target is greater than middle element, binary search right half of the array.
![[Pasted image 20240206123013.png||250]]
### Master Approach  

```js
function linearSearch(arr, target) {
   let leftIndex = 0;
   let rightIndex = arr.length - 1;
   
   while (leftIndex <= rightIndex) {
      let middleIndex = Math.floor((leftIndex + rightIndex) / 2)
      if (arr[middleIndex] === target) {
         return middleIndex;
      }

      if (arr[middleIndex] < target) {
         leftIndex = middleIndex + 1
      } else {
         rightIndex = middleIndex - 1
      }

   }
   return -1
}

// BIG-O NOTATION O(logn) 
```


![[Pasted image 20240206130323.png]]




1-04












