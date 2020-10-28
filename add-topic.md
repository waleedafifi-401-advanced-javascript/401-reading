# Redux - Additional Topics


## Questions
1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
- I could use redux-thunk and mapDispatchToProps to inject fetchDepartments to the stateless component and implement componentWillMount or similar lifecycle method, to load data - but then I don't need to pass the list via props, as the component would always load data for himself, and I don't want that, because whenever a new component is created the data is fetched from api instead of store...

- Another advice I've seen is to use getComponent function from react-router, and retreive all data before returning the component, however, I am not sure if it's the correct redux way, as I don't see how to use redux-thunk there, and logic kind of seems littered all accross the files, when it's the data required for only one component.

2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
- When you call an asynchronous API, there are two crucial moments in time: the moment you start the call, and the moment when you receive an answer (or a timeout).

- Each of these two moments usually require a change in the application state; to do that, you need to  dispatch normal actions that will be processed by reducers synchronously. Usually, for any API request you'll want to dispatch at least three different kinds of actions:

- An action informing the reducers that the request began.

- The reducers may handle this action by toggling an isFetching flag in the state. This way the UI knows it's time to show a spinner.

- An action informing the reducers that the request finished successfully.

- The reducers may handle this action by merging the new data into the state they manage and resetting isFetching. The UI would hide the spinner, and display the fetched data.

- An action informing the reducers that the request failed.

- The reducers may handle this action by resetting isFetching. Additionally, some reducers may want to store the error message so the UI can display it.

## Terms
1. **middleware** Middleware provides a way to interact with actions that have been dispatched to the store before they reach the store's reducer. Examples of different uses for middleware include logging actions, reporting errors, making asynchronous requests, and dispatching new actions.

2. **thunk** is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the body of the function once the asynchronous operations have completed
