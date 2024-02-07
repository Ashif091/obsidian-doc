### Problem 
- Given an array of integers, sort the array.
   - `const arr = [-6, 20, 8, -2, 4]`
   - `InsertionSort(arr) => Should return [-6, -2, 4, 8, 20]`
  ﻿

### Insertion sort idea
- Virtually split the array into a sorted and an unsorted part
- Assume that the first element is already sorted and remaining elements are unsorted
- Select an unsorted element and compare with all elements in the sorted part
- If the elements in the sorted part is smaller than the selected element, proceed to the next element in the unsorted part. Else, shift larger elements in the sorted part towards the right.
- Insert the selected element at the right index
- Repeat till all the unsorted elements are placed in the right order
﻿

![[Pasted image 20240206222744.png]]

### Master Approach  

```js
function InsertionSort(arr) {
 for (let i = 0; i < arr.length; i++) {
   let numberToinsert = arr[i];
   let j = i - 1 ;
   
   while(j >=0 & arr[j] > numberToinsert){
      arr[j+1] = arr[j]
      j = j-1
   }
   arr[j+1] = numberToinsert
 }
}
// BIG-O NOTATION O[N^2] 
```

