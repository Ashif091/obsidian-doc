   
- Destructuring in Node.js is a convenient way to extract values from objects or arrays and assign them to variables in a concise and readable manner. It simplifies the process of accessing nested properties or elements and helps avoid repetitive code.
-
```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
};

// Destructuring object properties
const { firstName, lastName, age } = person;

console.log(firstName);  // Output: John
console.log(lastName);   // Output: Doe
console.log(age);        // Output: 30

```
