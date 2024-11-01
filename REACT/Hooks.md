**Hooks allow function components to have access to state and other React features.**
**Hooks allow us to "hook" into React features such as state and lifecycle methods**

## Hook Rules

There are 3 rules for hooks:

- Hooks can only be called inside React function components.
- Hooks can only be called at the top level of a component.
- Hooks cannot be conditional

# examples

1. **useState**: Allows functional components to manage local state. It returns a stateful value and a function to update that value, similar to `this.state` and `this.setState()` in class components.
    
2. **useEffect**: Enables performing side effects in function components, such as data fetching, subscriptions, or manually changing the DOM. It runs after every render and replaces lifecycle methods like `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` in class components.
    
3. **useContext**: Provides a way to access the nearest context object within a functional component. It allows components to consume values from a context without needing a consumer component.
    
4. **useReducer**: An alternative to `useState` for managing complex state logic. It is usually preferable when state transitions follow more complex logic or involve multiple sub-values.
    
5. **useRef**: Returns a mutable ref object whose `.current` property is initialized to the passed argument. It is useful for accessing the DOM or storing mutable values across renders without causing re-renders.
    
6. **useMemo**: Memoizes the result of a function so that the result is cached and only recomputed when one of the dependencies has changed. It is useful for optimizing performance by preventing unnecessary re-renders.
    
7. **useCallback**: Returns a memoized callback function. It is similar to `useMemo` but specifically for memoizing functions.
    
8. **useLayoutEffect**: Similar to `useEffect`, but it fires synchronously after all DOM mutations. It is useful for scenarios where the effect needs to be executed synchronously in order to measure DOM nodes or perform other synchronous tasks.
    
9. **useImperativeHandle**: Customizes the instance value that is exposed to parent components when using `ref`. It is used to hide some of the internal logic of a component from its parent components.