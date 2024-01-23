- In JavaScript, the rest operator (`...`) is used in function parameters to gather all remaining arguments into a single array. It allows you to pass an arbitrary number of arguments to a function, which are then collected into an array.

```js
function sum(...numbers) {
  let total = 0;
  for (const num of numbers) {
    total += num;
  }
  return total;
}

console.log(sum(1, 2, 3)); // Outputs: 6
console.log(sum(5, 10, 15, 20)); // Outputs: 50

```
**Rest Operator (`...`):**

- **Usage**: The rest operator is used in function parameter lists to collect the remaining arguments into an array.
    
- **Use Case**:
    
    - It allows a function to accept a variable number of arguments without explicitly defining them as individual parameters.
- **Example**:
    

```js
    
    function sum(...numbers) {
       return numbers.reduce((total, num) => total + num, 0); } 
        const result = sum(1, 2, 3, 4); // The rest operator collects all arguments (
```

page id =  293