![[Pasted image 20230821163243.png|325]]
- when we assign an obj to another one, the two obj are represented same memory 

- the solution of this is 
 ![[Pasted image 20230821163959.png|350]]



```js
const x = {
    name : 'ashif ali ' //module.exports
}
  
let y = x;
 y = {
   name : 'adil' // only exports
 }
  
console.log(x)
console.log(y)
```

- if u export some function (only export)
- if try u export some obj (module.export)

1. **`module.exports`:**
    - `module.exports` is a reference to the object that is actually returned as the result of a `require` call for a given module.
    - You can directly assign an object, a function, a class, or any value to `module.exports`.

Example:



```js
// moduleA.js
module.exports = { 
someFunction: () => {
// ...  
} };
```

2. **`exports`:**
    - `exports` is an alias for `module.exports`. It points to the same object as `module.exports`.
    - However, you can't directly reassign `exports` to a new object. If you do so, it breaks the reference between `exports` and `module.exports`.

Example:



```js
// moduleB.js 
exports.anotherFunction = () => {  
// ... 
};  // This will not work as expected, breaking the reference between exports and module.exports
exports = {   someValue: 42 };
```











id=13