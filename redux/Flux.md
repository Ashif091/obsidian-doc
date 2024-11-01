>[!note]
>Flux is an architectural pattern used for building user interfaces, particularly in web applications.
>

- Flux emphasizes unidirectional data flow, meaning that data flows in a single direction through your application.

>[!warning]
>It is not a library nor a framework.

In a Flux architecture, data flows through the following components:

1. **Actions**: Actions are plain JavaScript objects that represent events or user interactions in the application. They are dispatched to the Dispatcher.
    
2. **Dispatcher**: The Dispatcher is a central hub that receives actions and dispatches them to registered callbacks (Stores).
    
3. **Stores**: Stores contain the application state and logic for handling actions. They register with the Dispatcher to receive actions, update their state, and emit change events.
    
4. **Views (React Components)**: Views are React components that subscribe to changes in Stores and update their UI accordingly. They dispatch actions in response to user interactions.