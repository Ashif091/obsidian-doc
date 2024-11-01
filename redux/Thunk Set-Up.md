First, you need to set up your Redux store with Redux Toolkit and apply the Redux Thunk middleware:

javascript


```js
store.js import { configureStore } from '@reduxjs/toolkit';
import thunk from 'redux-thunk'; 
import rootReducer from './reducers'; 
const store = configureStore({   reducer: rootReducer,   middleware: [thunk] });  export default store;
```

Next, you can create your Redux slice and define your action creators using Redux Toolkit:


```js
// counterSlice.js
import { createSlice } from '@reduxjs/toolkit';

const counterSlice = createSlice({
  name: 'counter',
  initialState: {
    value: 0,
    loading: false,
    error: null
  },
  reducers: {
    increment: state => {
      state.value++;
    },
    decrement: state => {
      state.value--;
    },
    incrementByAmount: (state, action) => {
      state.value += action.payload;
    },
    fetchDataRequest: state => {
      state.loading = true;
      state.error = null;
    },
    fetchDataSuccess: (state, action) => {
      state.loading = false;
      state.value = action.payload;
    },
    fetchDataFailure: (state, action) => {
      state.loading = false;
      state.error = action.payload;
    }
  }
});

export const {
  increment,
  decrement,
  incrementByAmount,
  fetchDataRequest,
  fetchDataSuccess,
  fetchDataFailure
} = counterSlice.actions;

export default counterSlice.reducer;

```

Then, you can create your Redux Thunk action creator:

```js
// actions.js
import { fetchDataRequest, fetchDataSuccess, fetchDataFailure } from './counterSlice';

export const fetchData = () => {
  return async dispatch => {
    dispatch(fetchDataRequest());
    try {
      const response = await fetch('https://api.example.com/data');
      const data = await response.json();
      dispatch(fetchDataSuccess(data));
    } catch (error) {
      dispatch(fetchDataFailure(error.message));
    }
  };
};

```
Finally, you can connect your React components to the Redux store using React Redux:

```jsx
// MyComponent.js
import React, { useEffect } from 'react';
import { useSelector, useDispatch } from 'react-redux';
import { fetchData, increment, decrement } from './actions';

const MyComponent = () => {
  const dispatch = useDispatch();
  const count = useSelector(state => state.counter.value);
  const loading = useSelector(state => state.counter.loading);
  const error = useSelector(state => state.counter.error);

  useEffect(() => {
    dispatch(fetchData());
  }, [dispatch]);

  return (
    <div>
      <h1>Counter: {count}</h1>
      {loading && <p>Loading...</p>}
      {error && <p>Error: {error}</p>}
      <button onClick={() => dispatch(increment())}>Increment</button>
      <button onClick={() => dispatch(decrement())}>Decrement</button>
    </div>
  );
};

export default MyComponent;

```