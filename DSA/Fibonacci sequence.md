
### Problem 
- Given a number 'n', find the first 'n' elements of the Fibonacci sequence. In mathematics, the Fibonacci sequence is a sequence in which each number is the sum of the two preceding ones. The first two numbers in the sequence are 0 and 1.
   - `fibonacci(2) = [0,1]`
   - `fibonacci(3) = [0,1,1]`
   - `fibonacci(7) = [0,1,1,2,3,5,8]`

#### My Approach

```js
function fibunacci (n){
    const fibonacciSqn = [0];    // RUN 1 
    for(let i = 1; i < n; i++){ 
        if(i === 1){
            fibonacciSqn.push(1); // RUN 1
        } else {  
            fibonacciSqn.push(fibonacciSqn[i-2] + fibonacciSqn[i-1]); // RUN n
        }
    }
    return fibonacciSqn; // RUN 1
} // LINE OF CODE RUN n+3
// BIG-O NOTATION O[N]
```

### Master Approach  

```js
function fibunacci (n){
    const fibonacciSqn = [0, 1];
    for(let i = 2; i < n; i++){
        fibonacciSqn[i] = fibonacciSqn[i-1] + fibonacciSqn[i-2]; 
    }
    return fibonacciSqn; 
} 
// BIG-O NOTATION O[N] (linear)
```



1-03