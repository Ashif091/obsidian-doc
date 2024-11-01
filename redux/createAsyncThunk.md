>[!tip]
>`createAsyncThunk` is a utility function provided by Redux Toolkit for creating asynchronous action creators in a standardized and simplified way.


Here's how `createAsyncThunk` works:

1. **Creating Async Actions**: With `createAsyncThunk`, you define an asynchronous action creator that represents an entire asynchronous operation, such as fetching data from an API.
    
2. **Automatic Action Types**: `createAsyncThunk` automatically generates three action types: pending, fulfilled, and rejected. These action types are based on the base action name provided to `createAsyncThunk`.
    
3. **Dispatching Actions**: When the asynchronous operation starts, `createAsyncThunk` dispatches a pending action with the payload containing the original arguments passed to the thunk function. Once the operation is completed, it dispatches either a fulfilled action with the resolved value or a rejected action with the error.
    
4. **Error Handling**: If the asynchronous operation fails (throws an error or returns a rejected promise), `createAsyncThunk` dispatches a rejected action with the error message as the payload.

[[createAsyncThunk set-Up]]
