  
>[!tip]
>Redux Toolkit is a official package for simplify the process of writing Redux logic in our applications by reduce boilerplate code

Some key features of Redux Toolkit include:

1. **configureStore**: function that combines several Redux-related settings and configurations into a single function call. 
    
3. **createSlice**: a function that generates Redux slice reducers. Slice reducers are a combination of action creators and reducer functions that handle updates to a specific slice of the Redux state.
    
5. **createAsyncThunk**:  a utility function  for creating asynchronous action creators. It simplifies the process of defining asynchronous logic in Redux, handling pending, fulfilled, and rejected action states automatically.
    
4. **createEntityAdapter**: This utility function creates a set of pre-defined reducer and selector functions for managing normalized data in the Redux store. It helps streamline common data management tasks, such as adding, updating, and deleting entities.
    
5. **Immer Integration**: Redux Toolkit integrates with the Immer library to simplify state updates in reducers. With Immer, we can write reducer logic that directly mutates state objects using a simple, immutable update syntax, making reducer code easier to read and write.