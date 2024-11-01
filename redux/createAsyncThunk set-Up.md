
```js
import { createAsyncThunk } from '@reduxjs/toolkit';
import { fetchUserData } from '../api/userApi';

export const fetchUser = createAsyncThunk(
  'user/fetchUser',
  async (userId, thunkAPI) => {
    try {
      const response = await fetchUserData(userId);
      return response.data;
    } catch (error) {
      return thunkAPI.rejectWithValue(error.message);
    }
  }
);

```

In this example:

- We use `createAsyncThunk` to define an asynchronous action creator called `fetchUser`.
- The first argument to `createAsyncThunk` is a base action name ('user/fetchUser') that will be used to generate the action types.
- The second argument is an asynchronous function that performs the actual data fetching operation. It receives the dispatched arguments (`userId`) and a `thunkAPI` object, which provides access to the dispatch method, getState function, and extra arguments passed to the thunk.
- Inside the async function, we use `fetchUserData` (an imaginary API function) to fetch user data based on the `userId`. If successful, we return the response data. If an error occurs, we use `thunkAPI.rejectWithValue` to return an action with the error message as the payload.