- React is a JavaScript library for building dynamic and interactive user interfaces.
    - In React applications, we don’t query and update the DOM. Instead, we describe our application using small, reusable components. React will take care of efficiently creating and updating DOM elements.                                      ![[Pasted image 20240401113042.png||300]]
    - React components can be created using a function or a class. Function-based components are the preferred approach as they’re more concise and easier to work with.![[Pasted image 20240401113138.png||200]]
    -  JSX stands for JavaScript XML. It is a syntax that allows us to write components that combine HTML and JavaScript in a readable and expressive way, making it easier to create complex user interfaces.
    - When our application starts, React takes a tree of components and builds a JavaScript data structure called the virtual DOM. This virtual DOM is different from the actual DOM in the browser. It’s a lightweight, in-memory representation of our component tree.
    - When the state or the data of a component changes, React updates the corresponding node in the virtual DOM to reflect the new state. Then, it compares the current version of virtual DOM with the previous version to identify the nodes that should be updated. It’ll then update those nodes in the actual DOM.
    - In browser-based apps, updating the DOM is done by a companion library called ReactDOM. In mobile apps, React Native uses native components to render the user interface.
    - Since React is just a library and not a framework like Angular or Vue, we often need other tools for concerns such as routing, state management, internationalization, form validation, etc.![[Pasted image 20240401161701.png]]



- React with [[TypeScript]] combines the power of React for building user interfaces with the type safety and static analysis capabilities of TypeScript. TypeScript is a superset of JavaScript that adds optional static typing to the language, allowing developers to catch type-related errors at compile-time rather than at runtime.


### [[Set Up➡️]] 
## [[Create a react project➡️]]

## [[Using terms➡️]]

## [[State Hooks ➡️]]
