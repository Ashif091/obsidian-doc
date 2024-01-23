
- In JavaScript, the spread operator (`...`) is a feature that allows you to expand or spread the elements of an iterable (like an array, string, or object) into various places, such as function arguments, array literals, or object literals. It's a versatile and powerful tool for manipulating and copying data.
- **Usage**: <span style="color:#00b0f0">The spread operator is used to spread elements of an array or properties of an object into another array or object.</span>
- 
3. **Passing Array Elements as Arguments:** You can pass array elements as individual arguments to a function.

```js 
function addNumbers(a, b, c)
{  
return a + b + c; 
} 
const numbers = [1, 2, 3]; 
const sum = addNumbers(...numbers); 
console.log(sum); // Outputs: 6
```

4. **Creating Copies of Objects:** You can use the spread operator to create shallow copies of objects.
```js

const originalObject = { x: 1, y: 2 };
const copiedObject = { ...originalObject }; 
console.log(copiedObject); // Outputs: { x: 1, y: 2 }

```


6. **Creating Arrays from Strings:** You can spread a string into individual characters to create an array.

javascriptCopy code

```js
const string = "hello"
const charArray = [...string];
console.log(charArray); // Outputs: ["h", "e", "l", "l", "o"]`
```



page id =  293

