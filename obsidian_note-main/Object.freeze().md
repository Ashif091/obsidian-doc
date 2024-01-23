- <span style="color:#00b0f0">is a method in JavaScript that is used to freeze an object, making it immutable. When an object is frozen, its properties cannot be added, removed, or modified.</span>

```js
const myObject = {
    prop1: 'value1',
    prop2: 'value2'
};

Object.freeze(myObject);

myObject.prop1 = 'new value'; // This assignment will be ignored in non-strict mode
console.log(myObject.prop1); // Output: 'value1'

delete myObject.prop2; // This deletion will be ignored in non-strict mode
console.log(myObject.prop2); // Output: 'value2'

myObject.prop3 = 'value3'; // This assignment will be ignored in non-strict mode
console.log(myObject.prop3); // Output: undefined

```
12*