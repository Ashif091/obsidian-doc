Indeed, an object in JavaScript is a collection of key-value pairs. The time complexity for various operations on objects can be described as follows:

1. **Insert (Addition) - O(1):**
   Adding a new key-value pair to an object typically has constant time complexity. The insertion operation is not affected by the size of the object.

2. **Remove - O(1):**
   Removing a key-value pair from an object also has constant time complexity. The removal operation is independent of the size of the object.

3. **Access - O(1):**
   Accessing the value associated with a specific key in an object is a constant-time operation. It directly retrieves the value without iterating over the entire object.

4. **Search - O(n):**
   Searching for a specific value within the values of an object has a time complexity of O(n). This is because it requires iterating over all values in the object until a match is found.

   - **Object.keys() - O(n):**
     The `Object.keys()` method returns an array of a given object's property names. As it involves iterating over all keys, its time complexity is O(n).

   - **Object.values() - O(n):**
     The `Object.values()` method returns an array of a given object's property values. Like `Object.keys()`, it also has a time complexity of O(n) as it iterates over all values.

   - **Object.entries() - O(n):**
     The `Object.entries()` method returns an array of a given object's own enumerable property [key, value] pairs. Its time complexity is O(n) since it involves iterating over all key-value pairs.

Given your example:

```js
const person = {
    firstName: 'Bruce',
    lastName: 'Wayne'
}
```

Operations on this `person` object align with the mentioned time complexities. Accessing or modifying the `firstName` or `lastName` properties, for example, would have constant time complexity (O(1)), while searching for a specific value would have linear time complexity (O(n)).


1-02