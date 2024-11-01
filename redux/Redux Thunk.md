
>[! Redux Thunk is a middleware package for Redux that allows it to handle asynchronous actions]
that enables us to write action creators that return functions . These functions can perform asynchronous operations, such as fetching data from an API, and dispatch additional actions once the asynchronous operation is complete.

1. **Action Creators**: With Redux Thunk, your action creators can return either plain action objects or functions. If a function is returned, Redux Thunk intercepts it and calls it with `dispatch` and `getState` as arguments.
    
2. **Async Logic**: Inside the action creator function, you can perform any asynchronous operations, such as making an HTTP request using `fetch` or `axios`. You can also perform any synchronous logic needed to prepare the action or handle the async response.
    
3. **Dispatching Additional Actions**: Once the async operation is complete, you can dispatch additional actions to update the Redux store based on the result of the async operation. These actions can be used to update the loading state, store fetched data in the Redux store, or handle errors.

[[Thunk Set-Up]]

