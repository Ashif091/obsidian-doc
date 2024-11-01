>[!React-Redux]
>It provides React components and utilities that allow our React components to interact with the Redux store

- React-Redux acts as a bridge between React components and the Redux state management system.
- It enables you to connect your React components to the Redux store, allowing them to access and update the application state stored in Redux.
---
1. This `<Provider>` component takes the Redux store as a prop and makes it available to all the components in our application.
```tsx
import { Provider } from 'react-redux';
import store from './store'; // Your Redux store

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root')
);
```

2. we can use the `connect` function provided by React-Redux to connect them to the Redux store. This function takes two arguments: `mapStateToProps` and `mapDispatchToProps`. It returns a higher-order component (HOC) that wraps your component, providing it with access to the Redux store.
```jsx
import { connect } from 'react-redux';

const MyComponent = ({ data, fetchData }) => {
  // Use data from Redux store
  // Call fetchData action creator
  
  return (
    // JSX of your component
  );
};

const mapStateToProps = state => ({
  data: state.data,
});

const mapDispatchToProps = dispatch => ({
  fetchData: () => dispatch(fetchDataAction()),
});

export default connect(mapStateToProps, mapDispatchToProps)(MyComponent);
```

3. **mapStateToProps**: This function maps a slice of the Redux state to props that are passed to our component. It allows our component to access specific parts of the Redux state and use them as props.

4. **mapDispatchToProps**: This function maps action creators to props that are passed to our component. It allows our component to dispatch actions to update the Redux state.

>[!warning]
>`connect` is a higher-order component (HOC) for class components.

----
>[!For the functional components]
>`useDispatch` and `useSelector` are hooks provided by the React-Redux library for functional components

1. **useDispatch**:
    - `useDispatch` is a hook that provides access to the Redux `dispatch` function.
    - It allows functional components to dispatch actions to the Redux store.
    - It's typically used within functional components to trigger state changes.
```jsx
import { useDispatch } from 'react-redux';

const MyComponent = () => {
  const dispatch = useDispatch();

  const handleClick = () => {
    dispatch({ type: 'INCREMENT' });
  };

  return (
    <button onClick={handleClick}>Increment</button>
  );
};

```

2. **useSelector**:
    - `useSelector` is a hook that allows functional components to extract data from the Redux store state.
    - It accepts a selector function as an argument, which returns the data from the Redux store.
    - It automatically subscribes to the Redux store, so the component will re-render whenever the selected data changes.
```jsx
import { useSelector } from 'react-redux';

const MyComponent = () => {
  const count = useSelector(state => state.count);

  return (
    <div>Count: {count}</div>
  );
};

```