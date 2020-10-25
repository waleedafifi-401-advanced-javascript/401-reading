## Props and State

1. Does a deployed React application require a server?
- Yes, you need a server to host a deployed React app. 

2. Why do we prefer to test a React application at the behavior rather than the unit level?
- We want to be testing the actual user experience not the components themselves. When this happens in the browser and it is then responsible for rendering something, we want to make sure that actually happens. 

3. What does `npm run build` do?
- Using this command will create a build directory with a production build of the app
- This is helpful because we have many js and scss files as we make components and modularize out, and when a user visits the site it would normally require additional HTTP requests for each of the files. To help with that you can create a build which merges CSS files into one, and same with JS. To do so you use a *build tool* and that is what `npm run build` is.

4. Describe the actual composition / architecture of a React application.
- A React app should have an entry point (file) that renders the React DOM root element that will hold all of the components we create. There should be a main App file that further nests the individual components and also provides general rules for styling the page as a whole. Next we can break out individual components and their styling to separate folders with files, importing them all into the main App file. 

## Vocabulary

|    **Term**    | **Definition**  |
| -------------- | ----------- |
| BDD | Behavior Driven Development  |
| Acceptance Tests | testing React and the behavior of the app, not individual components. based off inspecting the DOM.  |
| mounting | (via Stack Overflow) process of outputtin the virtual representation of a component into the final UI representation... outputting a React element into an actual DOM element |
| build | the compiling of all the files in a project to be able to go to production |
