- .ts use for creating a typescript file , .tsx for creating a react components 
- we can create the react components in two  way 
    - js class 
    - js function 

- the functional components are more popular .so we use javaScript function instead of class
- For naming we follow the [PascalCasing](https://www.theserverside.com/definition/Pascal-case) format 

#### first component 
```tsx
function Message(){
    let name = "Ashf"
    return <h1>Hi {name.toUpperCase()}</h1>
}
export default Message ;
```

#### Working 

Message -> App -> 
![[Pasted image 20240401125641.png||400]]
1. **Component-based Architecture**: React applications are built using reusable components, which are small, self-contained units of code that represent a part of the user interface. Each component can have its own state and properties (props).
    
2. **Rendering**: When a React application is initially loaded or when its state changes, React builds a virtual representation of the UI called the Virtual DOM. This is a lightweight, in-memory representation of the actual DOM.
    
3. **Virtual DOM**: The Virtual DOM is a tree structure that mirrors the structure of the actual DOM but contains only JavaScript objects. This allows React to perform updates to the UI more efficiently.
    
4. **Reconciliation**: When the state of a component changes, React performs a process called reconciliation to update the Virtual DOM. React compares the new Virtual DOM with the previous one and identifies the differences (or "diffs") between them.
    
5. **Minimal DOM Updates**: React determines the minimal set of changes needed to update the actual DOM based on the differences identified during reconciliation. This process is highly efficient because React minimizes the number of updates to the real DOM, which can be costly in terms of performance.
    
6. **Batching Updates**: React batches multiple updates to the Virtual DOM and applies them in a single pass to the actual DOM. This helps reduce unnecessary re-renders and improves performance.
    
7. **Component Lifecycle**: React components have lifecycle methods that allow developers to hook into various stages of a component's life, such as initialization, rendering, updating, and unmounting. These lifecycle methods provide opportunities to perform actions like fetching data, updating state, or cleaning up resources.
    
8. **State Management**: React uses a unidirectional data flow, where data flows from parent components to child components via props. State management libraries like Redux or React Context API can be used to manage application state more effectively, especially in larger applications with complex data requirements.

![[Pasted image 20240401161852.png||300]]


