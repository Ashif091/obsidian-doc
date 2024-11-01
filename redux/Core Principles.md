Redux can be described in three fundamental principles

>[!1.Single Source of Truth]
>The entire state of our application is stored in a single JavaScript object, known as the state tree or state container. This makes it easy to access and manipulate the state of your application from a centralized location.

>[!2.State is Read-Only]
>The state object is immutable and cannot be changed directly. The only way to modify the state is by dispatching actions

>[!3.Changes are Made with Pure Functions]
>To describe how the state tree is transformed by actions, we write pure reducer functions. These functions take the previous state and an action as arguments, and return the new state. `Reducers must be pure functions`, meaning they produce the same output for the same input and have no side effects.


------

>[!4.Changes are Made by Dispatching Actions]
>Actions are the only way to modify the state in Redux. They are plain JavaScript objects that must have a `type` property indicating the type of action being performed. we can also include additional data in the action object to provide information about what should change in the state.

>[!5.Unidirectional Data Flow]
>Data flows in a single direction through your application: from the state container to the UI components. Any changes to the state trigger a re-render of the UI components that are subscribed to the relevant parts of the state
