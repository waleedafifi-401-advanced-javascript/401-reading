![](https://i.morioh.com/8c8203b86e.png)

## Express

### Express Routing
* This is an event driven system
* Same routing patter as vanilla JS and JQuery
* When a get event happens on "/thing", run this function...
* The **request** object will accept Parameters and Query Strings
* The **response** object is responsible for sending data back to browser
* Responses include headers, cookies, and status codes


### Event driven system
- app.get('/thing', (req,res) => {})

### The Request Object
- (req,..)
- :parameters
    - app.get('/api/:thing',...) = req.params.thing
- Query Strings
    - http://server/route?ball=round = req.query.ball
### The Response Object
- (..., res)
- Responsible for sending data back to the browser
- Has methods like send() and status() that Express uses to format the output to the browser properly
    - Sends Headers
        - Cookies
        - Status Codes


### Express Middleware
* Middleware is a series of functions that the request moves through
* Each receives **request, response and next** as parameters
* Two types - Application and Route
* **Application**
  * Error handling
  * Bringing in other routes
  * Applies Defaults
  * JSON, Body and Form parsing
  * Runs on every request
* **Route**
  * Specifically for a route
  * Are you logged in?
  * What is your IP?
  * Have we seen you here before?

### Modularization & Separation of Concerns
* Modularize code into logical chunks
* Each thing should do the thing it is best at

### CRUD Operations with REST and Express
* CREATE - app.post('/resource')
* READ - app.get('/resource')
* UPDATE - app.put('/resource/:id')
* DELETE - app.get('/resource/:id')

### Server Testing
* Avoid starting actual server for testing
* Export server as a module in a library
* Use **supertest** to run tests
  * Hits routes as though server is running without starting it
  * One less thing to go wrong (eliminate variables)
* Wrap **superagent** in a module that persons this
  * 100% fake every call to the API
  * Only tests the interface to the API, not actual data

### Test Pyramid
* Server Testing
  * Units - Server Internal Functions
    * Mock integrations
  * Integration - How it connects to other services
    * Hard dependencies
  * Acceptance
    * Server might be a dependency of another test

### What is Middleware?
  * Functions invoked by the Express.js routing layer before final request handler is made
  * On a route, do something first, then pass it along to the next function
  * Request and Response used each time to pass to the next whatever it is being handled
  * Deal with CORS or CSRF issues first, check to see if user is authorized, and then send them where they want to go
  * **App.use** runs middleware on all requests
  * Can declare middleware functions wherever in file due to hoisting


## Vocabulary Terms
| Term | Definition |
|-|-|
| SOAP | SOAP (abbreviation for Simple Object Access Protocol) is a messaging protocol specification for exchanging structured information in the implementation of web services in computer networks |
| ReST Verbs | REST verbs specify an action to be performed on a specific resource or a collection of resources. When a request is made by the client, it should send this information in the HTTP request |
| CRUD Verbs | HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE |
| Swagger | Swagger is a set of rules (in other words, a specification) for a format describing REST APIs. ... As a result, |