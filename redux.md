# Application State with Redux

## Redux 
**Redux** is an **open-source** JavaScript library for managing application state. It is most commonly used with libraries such as React or Angular for building user interfaces. Similar to Facebook's Flux architecture, it was created by ***Dan Abramov*** and ***Andrew Clark***.

#### Is Redux immutable?
Redux is a small library that represents state as (**immutable**) objects. And new states by passing the current state through pure functions to create an entirely new object/application states. ... State of your app is only changed by a category of pure functions called **reducers**.


### Benefits Of Redux
1. Predictability of outcome
   - There is always one source of truth, the store, with no confusion about how to sync the current state with actions and other parts of the application.

2. Maintainability
   - Having a predictable outcome and strict structure makes the code easier to maintain.

3. Organization
   - Redux is stricter about how code should be organized, which makes code more consistent and easier for a team to work with.

4. Server rendering
   - This is very useful, especially for the initial render, making for a better user experience or search engine optimization. Just pass the store created on the server to the client side.

5. Developer tools
   - Developers can track everything going on in the app in real time, from actions to state changes.

6. Community and ecosystem
   - This is a huge plus whenever you’re learning or using any library or framework. Having a community behind Redux makes it even more appealing to use.

7. Ease of testing
   - The first rule of writing testable code is to write small functions that do only one thing and that are independent. Redux’s code is mostly functions that are just that: small, pure and isolated.

### Functional Programming
- It is able to treat functions as first-class objects.
- It is able to pass functions as arguments.
- It is able to control flow using functions, recursions and arrays.
- It is able to use pure, recursive, higher-order, closure and anonymous functions.
- It is able to use helper functions, such as map, filter and reduce.
- It is able to chain functions together.
- The state doesn’t change (i.e. it’s immutable).
- The order of code execution is not important.

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56797aa4-a483-41ea-97e4-8b9280464fd1/01-functional-programming-opt-preview.png)


### Questions

1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”
   - Not as vulnerable to XSS attack because a cookie isn't accessible via JavaScript
      - XSS is cross-site scripting which enables attackers to inject client-side javascript into web pages viewed by others. Often used to bypass access controls.

2. Explain 3rd party cookies.
   - 3rd party cookies are those that are established by domains other than the one you're on. Used mainly for tracking and online-advertising.

3. How do pixel tags work?
   - Pixel tag is a tiny snippet of code that allows you to gather info about website users. Usually a small img that contains code to an external link (the pixel server). If/when user visits the destination site the code is processed by the client, the user's browser. Browser follows link, opens graphic, which is registered and noted in server's log files

## Vocabulary
| **Term** | **Definition** |
| ---- | ---------- |
| cookies |	small files located on user's computer designed to hold data specific to client and website, so it can be accesses by either web server or client computer allows server to deliver page tailored to user, designed to carry info from one visit to the site to the next |
| authorization | the thing received when an access token is verified |
| access control | the practice of restricing access in specific ways to a resource based on your user status, an example being RBAC |
| conditional rendering | the go-ahead of rendering certain components that have all the behavior you need, when the specific conditions are true (can use operators like if and conditional operator) |
| Redux | JS library for managing application state |
