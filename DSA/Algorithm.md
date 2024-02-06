---
date created: 2024-01-30 22:31
date updated: 2024-01-30 22:32
---

## What is an Algorithm?

input -> algorithms -> output

#### Characteristics

1. Well defined inputs and outputs
2. Each step should be clear and unambiguous
3. Language independent

## Why algorithms?

1. As a developer, you're going to come across problems that you need to solve
2. Learning algorithms translates to learning different techniques to efficiently solve those problems
3. One problem can be solved in many ways using different algorithms
4. Every algorithm comes with its own tradeoffs when it comes to performance

## Algorithm analysis

1. There are multiple ways to solve one problem (e.g., multiple algorithms to sort a list of numbers)
2. How do we analyze which one of them is the most efficient algorithm?
3. Generally, when we talk about performance, we use an absolute measure
4. If I can run 100 meters in 12 seconds, I'm faster than someone who takes 15 seconds

## Algorithm analysis contd.

1. The absolute running time of an algorithm cannot be predicted, as it depends on various factors
   - Programming language used to implement the algorithm
   - The computer the program runs on
   - Other programs running at the same time
   - Quality of the operating system
2. We evaluate the performance of an algorithm in terms of its input size
   - Time complexity: Amount of time taken by an algorithm to run, as a function of input size
   - Space complexity: Amount of memory taken by an algorithm to run, as a function of input size
3. By evaluating against the input size, the analysis is machine-independent and provides a more appropriate comparison
   - There is no one solution that works every single time. It is always good to know multiple ways to solve the problem and use the best solution given your constraints
   - If your app needs to be very quick and has plenty of memory to work with, you don't have to worry about space complexity
   - If you have very little memory to work with, you should pick a solution that is relatively slower but needs less space

## How to represent complexity?

### Asymptotic notations

Mathematical tools to represent time and space complexity
1.  [[Big O notation]] (O-notation) - Worst case complexity
2. Omega Notation (Ω-notation) - Best case complexity
3. Theta Notation (Θ-notation) - Average case complexity


1-00