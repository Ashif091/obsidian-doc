### Problem
- Given a sorted array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.
   - `arr =  [-5, 2, 4, 6, 10], t = 10 -> Should return 2`
   - `arr = [-5, 2, 4, 6, 10], t = 6 -> Should return 4`
   - `arr = [-5, 2, 4, 6, 10], t = 20 -> Should return -1`

### Tips for Recursive binary search
_______________
- Figure out how to break down the problem into smaller versions of the same problem
- Identify the base case for recursion

```js
const arr = [-5, 2, 4, 6, 10];

function linearSearch(arr, target) {

   return search(arr, target, 0, arr.length - 1)

}

  

function search(arr, target, leftIndex, rightIndex) {
   if (leftIndex > rightIndex) {
      return -1
   }

   let middleIndex = Math.floor((leftIndex + rightIndex) / 2)
   if (arr[middleIndex] === target) {
      return middleIndex;
   }

   if (arr[middleIndex] < target) {
      return search(arr, target, middleIndex + 1, rightIndex)
   } else {
      return search(arr, target, leftIndex, middleIndex - 1)
   }

}
//big-O O(logn)
```


1-04