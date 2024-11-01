>[!Immer is a JavaScript library that provides a simpler way to work with immutable data structures by allowing we to write code that looks like it's mutating state directly, even though it's producing a new immutable state behind the scenes.]
>  
***In the context of Redux, Immer is often used in combination with Redux Toolkit or directly within Redux reducers to simplify state updates***

- Redux Toolkit's [`createReducer`](https://redux-toolkit.js.org/api/createReducer) and [`createSlice`](https://redux-toolkit.js.org/api/createSlice) automatically use [Immer](https://immerjs.github.io/immer/) internally to let you write simpler immutable update logic using "mutating" syntax.

>[!tip]
>**In order to update values immutably, your code must make _copies_ of existing objects/arrays, and then modify the copies**.