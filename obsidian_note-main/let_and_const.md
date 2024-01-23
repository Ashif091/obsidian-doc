`let` and `const` are two ways to declare variables in JavaScript introduced in ECMAScript 6 (ES6). They provide more controlled and predictable ways to manage variables compared to the older `var` keyword.

1. **`let` Declaration:**
    
    - The `let` keyword is used to declare variables that can be reassigned with new values.
    - 
2) **`const` Declaration:**

- The `const` keyword is used to declare variables that are constant, meaning their values cannot be changed once assigned.
## Temporal Dead Zone
The "Temporal Dead Zone" in JavaScript is a phase between when a variable is declared using `let` or `const` and when it's actually assigned a value. During this phase, if you try to access the variable, you'll get an error. This concept helps catch potential issues with using variables before they are properly initialized, improving code reliability.



#### the script storage 
- the let and const are save here.
- we can't locate this from the window or this 

## const 
```js
const a;
a= 100; // it **is type error**
❌----------------we can't do that'--------

✔️  const a = 200;

```
