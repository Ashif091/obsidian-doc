### Problem 
- Given an array of integers, sort the array.
   - `const arr = [-6, 20, 8, -2, 4]`
   - `bubbleSort(arr) => Should return [-6, -2, 4, 8, 20]`
  

### idea
- Compare adjacent elements in the array and swap the positions if they are not in the intended order
- Repeat the instruction as you step through each element in the array
- Once you step through the whole array with no swaps, the array is sorted

### logic
```scss
[-6 20 8 -24]
[-6 20 8 -2 4 ] → [ -6 8 20 -2 4 ] Swap since 20 > 8
[-6 8 20-24] → [ -6 8 -2 20 4 ] Swap since 20 > -2
[-6 8-2 204] → [ -6 8 -2 4 20 ] Swap since 20 > 4
End of array. Elements swapped? Yes? Repeat the comparison. [-68-24 20]
[-6 8-24 20 ] →→ [ -6 -2 8 4 20 ] Swap since 8 > -2
[-6-28 4 20] → [-6-2 4 8 20 ] Swap since 8 > 4
[-6-2 4 8 20]
End of array. Elements swapped? Yes? Repeat the comparison.
[-6-2 4 8 20 ] [ -6 -2 4 8 20 ] [ -6 -2 4 8 20 ] [ -6 -2 4 8 20]
End of array. Elements swapped? No? Array is sorted.
```



#### My Approach

```js
  

function bubbleSort(arr){
   for (let i = 0; i < arr.length; i++) {
      for (let j = 0; j < arr.length-1-i; j++) {
       if(arr[j] > arr[j+1]){
         let temp = arr[j]
         arr[j] = arr[j+1]
         arr[j+1] = temp
       }
      }
   }
   return arr;
}
// BIG-O NOTATION  O[N^2] 
```

### Master Approach  

```js
function bubbleSort(arr) {
   let swapped ;
   do {
      swapped = false ;
      for (let j = 0; j < arr.length - 1; j++) {
         if (arr[j] > arr[j + 1]) {
            swapped = true ;
            let temp = arr[j]
            arr[j] = arr[j + 1]
            arr[j + 1] = temp
         }
      }
   } while (swapped);
   return arr;
}
// BIG-O NOTATION O[N^2] 
```


