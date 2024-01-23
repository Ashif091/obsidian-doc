**Shallow Copy:** <span style="color:#00b0f0">Shallow copying creates a new object or array that is a copy of the original, but it only copies the top-level structure. If the original object or array contains nested objects or arrays, those nested structures are not deeply copied</span>; instead, references to the nested structures are maintained in the copied object or array. In other words, changes made to the nested structures in the original will be reflected in the copied object or array, and vice versa.

Shallow copying methods include techniques like using the spread operator (`...`), the `Object.assign()` method, and array methods like `slice()` or `concat()`.


```js
// Shallow copy example 
const originalArray = [1, [2, 3]]; 
const shallowCopyArray = [...originalArray];  // or originalArray.slice();

```


























12*