### Algorithmic Complexity and Big-O Notation

Big-O notation is a vital tool for analyzing and describing the efficiency of algorithms in terms of their worst-case complexity. It is characterized by two key aspects:

1. **Expression in terms of the Input:**
   Big-O notation provides a concise way to express how the runtime of an algorithm scales concerning the size of the input. The notation, such as O(n), signifies the upper bound of the algorithm's growth rate concerning the input size.

﻿![[Pasted image 20240131091954.png]]

2. **Focus on the Bigger Picture:**
   Big-O notation enables us to concentrate on the overall efficiency of an algorithm without delving into minute implementation details. This abstraction helps in comparing algorithms and making informed decisions about their suitability for specific tasks.

   ![[Pasted image 20240131092241.png||400]]

### Time Complexity O(n) - Linear

```js
function summation(n) {
    let sum = 0;
    for (let i = 1; i <= n; i++) {
        sum += i;
    }
    return sum;
}
```

The time complexity of this algorithm is O(n), indicating a linear relationship between the input size (n) and the runtime. As the input grows, the runtime grows linearly.

### Time Complexity O(1) - Constant

```js
function summation(n) {
    return (n * (n + 1)) / 2;
}
```

This algorithm's time complexity is O(1), reflecting constant time regardless of the input size. It achieves efficiency by directly computing the result without the need for iteration.

### Time Complexity O(logn) - Logarithmic

Logarithmic time complexity, O(logn), is characteristic of algorithms where the runtime grows at a slower rate than the input size increases. It is efficient and often associated with divide-and-conquer strategies.

### Key Points to Note:

- Multiple algorithms may exist for the same problem, each with its strengths and weaknesses.
- Different algorithms excel under different constraints; the optimal choice depends on the specific use case.
- The same algorithm, implemented in the same programming language, can take different forms.
- Prioritize code simplicity and readability in professional settings; clarity often outweighs cleverness in the long run.


[[Objects - Big-O]]

[[Array - Big-O]]



![[Pasted image 20240203160731.png]]





1-00