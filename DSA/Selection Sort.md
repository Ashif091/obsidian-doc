### Problem

- Given an array of integers, sort the array.
    - `const arr = [-6, 20, 8, -2, 4]`
    - `SelectionSort(arr) => Should return [-6, -2, 4, 8, 20]`

### Selection Sort Idea

- Start by assuming the first element is the smallest in the array.
- Compare the current element with the rest of the array.
- If a smaller element is found, mark its position.
- Once the entire array has been scanned, swap the current element with the smallest element found.
- Move to the next element and repeat the process until the array is sorted.

### Master Approach

```js
function SelectionSort(arr) {
    
    for (let i =  0; i < arr.length; i++) {
        let minIndex = i;
        for (let j = i +  1; j < arr.length; j++) {
            if (arr[minIndex] > arr[j]) {
                minIndex = j;
            }
        }
        // Swap elements
        if (minIndex != i) {
            let temp = arr[i];
            arr[i] = arr[minIndex];
            arr[minIndex] = temp;
        }
    }
}
// BIG-O NOTATION O[N^2]  

```


### Key Points

- Selection sort is an in-place, comparison-based algorithm.
- It is not stable, meaning equal elements may not retain their original order.
- Suitable for small lists due to its simplicity and low overhead.
- Has a worst-case and average time complexity of O(n^2), where n is the number of elements in the list.