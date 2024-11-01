## Fragment 
  
In React, a #fragment is a built-in component that allows you to group multiple children elements without adding an extra DOM element. Fragments are useful when you need to return multiple elements from a component, but you don't want to wrap them in a parent element like a `<div>`.
```tsx
import React from 'react';

const MyComponent = () => {
  return (
    <>
      <h1>Hello</h1>
      <p>This is a paragraph.</p>
    </>
  );
};

export default MyComponent;

```

## [[Hooks]]
  
In React, a hook is a special function that allows you to use state and other React features in function components. Hooks were introduced in React 16.8 as a way to use stateful logic and side effects in functional components, which were previously only possible in class components.
```js
import React, { useState } from 'react';

function Example() {
  // Declare a state variable named "count" with an initial value of 0
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
export default Example;

```


### State
State is built-in feature that allows components to keep track of information that can change over time. It represents the dynamic data in a component. State is mutable and can be changed within the component. `As the introduction of hooks we can now use state in functional components also`. In class component state is accessed using `this.state.stateVariableName`
## props

In React, props (Properties)  are a way to pass data from a parent component to child component. They allow you to make components dynamic and reusable. Props are read-only, which means that the child components receiving props cannot modify the props they receive. In stateful component you have get the data from

```tsx
// ChildComponent.jsx
import React from 'react';

function ChildComponent(props) {
  return (
    <div>
      <p>Name: {props.name}</p>
      <p>Age: {props.age}</p>
    </div>
  );
}
export default ChildComponent;
```

## [props 🆚 state](https://www.geeksforgeeks.org/reactjs-state-vs-props/)

![[Pasted image 20240402131340.png]][State](https://www.geeksforgeeks.org/reactjs-state-react/) in React:

A state is a variable that exists inside a component, that cannot be accessed and modified outside the component, and can only be used inside the component. Works very similarly to a variable that is declared inside a function that cannot be accessed outside the scope of the function in normal javascript. State ****Can be modified using this.setState. The state can be asynchronous****. Whenever this.setState is used to change the state class is rerender itself. :

 [Props](https://www.geeksforgeeks.org/reactjs-props-set-1/) in React:

React allows us to pass information to a Component using something called props (which stands for properties). Props are objects which can be used inside a component. Sometimes we need to change the content inside a component. Props come to play in these cases, as they are passed into the component and the user..


|****PROPS****|****STATE****|
|---|---|
|The Data is passed from one component to another.|The Data is passed within the component only.|
|It is Immutable (cannot be modified).|It is Mutable ( can be modified).|
|Props can be used with state and functional components.|The state can be used only with the state components/class component (Before 16.0).|
|Props are read-only.|The state is both read and write.|

## state hooks
![[Pasted image 20240402211126.png||400]]
## update state 
- example 1 
![[Pasted image 20240402213815.png||500]]
- example 2
![[Pasted image 20240402214026.png||500]]
- example 3
![[Pasted image 20240402214514.png||500]]
- example 4
![[Pasted image 20240402230234.png||500]]
- example 5 (array updation )
![[Pasted image 20240402231912.png||500]]
- example 6 
![[Pasted image 20240403095729.png||500]]
- example 7
## Strict Mode 
  
In React, Strict Mode is a development mode feature that helps highlight potential problems and inconsistencies in your application's code. When enabled, Strict Mode performs additional checks and warnings during rendering and helps identify unsafe practices and potential bugs early in the development process.

## [useEffect](https://www.w3schools.com/react/react_useeffect.asp)
The `useEffect` Hook allows you to perform side effects in your components.
Some examples of side effects are: fetching data, directly updating the DOM, and timers.
`useEffect` accepts two arguments. The second argument is optional.
`useEffect(<function>, <dependency>)`
##### Example

1. No dependency passed:

```jsx
useEffect(() => {
  //Runs on every render
});
```

##### Example

2. An empty array:

```jsx
useEffect(() => {
  //Runs only on the first render
}, []);
```

##### Example

3. Props or state values:

```jsx
useEffect(() => {
  //Runs on the first render
  //And any time any dependency value changes
}, [prop, state]);
```


