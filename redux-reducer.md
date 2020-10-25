# Redux - Combined Reducers

1. Why choose Redux instead of the Context API for global state?
- As an application scales it is easier to control individual pieces of state by using Redux. Its an easier way to drill into props.

2. What is the purpose of a reducer?
- A reducer is a function that determines changes to an application's state. It grabs the action, deconstructs it, and uses it to determine the change and what to do with it.

3. What does an action contain?
- An action should contain a type and a payload, and while these names are set in stone it's the naming convention and should be stuck to. You can peel off the type and payload from the action object and use them to initiate dispatches.

4. Why do we need to copy the state in a reducer?
- Because we want to always be dealing with unmutated state, so we need to make a copy of it with the new thing that we are altering in the relevant part of the reducer.

## Vocabulary
| **Term**	| **Definition** |
| ----- | ---------- |
| immutable state	| is an object whose state cannot be modified after it is created. This is in contrast to a mutable object (changeable object), which can be modified after it is created. |
| time travel in redux	| is the ability to move back and forth among the previous states of an application and view the results in real time. With Redux, given a specific state and a specific action, the next state of the application is always exactly the same. |
| action creator	| is merely a function that returns an action object. ... Calling an action creator does nothing but return an object, so you have to either bind it to the store beforehand, or dispatch the result of calling your action creator |
| reducer	| is a function that determines changes to an application's state. It uses the action it receives to determine this change. ... Redux relies heavily on reducer functions that take the previous state and an action in order to execute the next state. We're going to focus squarely on reducers is in this post |
| dispatch	| is a function of the Redux store. You call store. dispatch to dispatch an action. This is the only way to trigger a state change. ... connect can accept an argument called mapDispatchToProps , which lets you create functions that dispatch when called, and pass those functions as props to your component |
