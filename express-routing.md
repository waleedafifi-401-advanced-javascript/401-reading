![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTJ9wysr-Cfmaf9vOPurnsAA2MJMuZUL0DFRQ&usqp=CAU)

# Express Routing


#### What Is Routing?
Routing is a method that refers to determining how an application responds to a client request to a particular path and a specific HTTP request method (GET, POST, and so on).

In simple terms, routing is controlling which function gets invoked whenever the user navigates to a particular URL. In this context, URL refers to any path or route.

#### Routing Methods
```
app.METHOD(PATH,CALLBACK)
```

* `get`: To handle GET requests (i.e. to request/GET data from a specified resource).
* `post`: To send data to a server to create/update a resource.
* `put`: To send data to a server to create/update a resource. The difference between POST and PUT requests is that the latter are idempotent. This means that PUT requests have no additional effect if they are called multiple times. In contrast, if you call a POST method more than once, your program will have side effects. Therefore, bear in mind that POST requests are not to be called more than once.
* `delete`: For removal of a specified resource.


#### Basic Examples
```
const express = require('express')
const app = express()

app.get('/', (req,res)=> { //get method
  res.send('Hello World') //send response
})
app.listen(3000)
```

To run this code, first go to a terminal window and type `node express-basic-hello-world`. Then, on another terminal, type curl localhost:3000.

![](https://miro.medium.com/max/1310/1*_KC67jtSV79R6yeLq2f_tQ.png)


#### express.Router()
We can use `express.Router()` to create modular, mountable route handlers. A Router instance is a complete middleware and routing system, which is why it is often referred to as a “mini-app.”


To use `app.Router()`, we have to create a separate module, instantiate an instance of `app.Router`, and then use `module.exports` to export the instance.

In below example wwee can use `router()` method aand then expoort thee routre to use it in another place

```
const express = require('express')
const router= express.Router()

router.route('/:username/:id')
    .get((req,res)=>{
        validateID(req.params.id);
    res.send(' welcome to page, ' + req.params.username)
})
    .post((req,res)=>{
    processData(req.params.username);
    res.send('data received ')
})

module.exports = router;
```

And use it aftre require it in anothre file like below
```
const express =require('express')
const routeExample = require('./routeExample')
const app = express()

app.use('/',routeExample); //use routeExample.js to handle routes starting with '/'
app.use('/cats',routeExample); //use routeExample.js to handle routes starting with '/cats'
app.use('/rabbits',routeExample); //use routeExample.js to handle routes starting with '/rabbits'

app.listen(3000);
```


#### Different routes in express.Router with middleware
In this example, we will navigate to the Birds homepage of our pet shop and define a middleware function, `timeLog`, which will output the time the respective path was requested.

```
var express = require('express')
var router = express.Router()

// middleware that is specific to this router
router.use(function timeLog (req, res, next) {
  console.log('Time: ', Date.now())
  next()
})
// define the home page route
router.get('/', function (req, res) {
  res.send('Birds home page')
})
// define the about route
router.get('/about', function (req, res) {
  res.send('About birds')
})

module.exports = router
```

```
var birds = require('./birds')
app.use('/birds', birds) //handle /birds and /birds/about
```

![](https://miro.medium.com/max/1250/1*kiKfmt2sqOFLRD1mIEIpyg.png)

![](https://miro.medium.com/max/1400/1*mk_5suqPWSy00qB6y5gmdQ.png)


#### Trems
| Term | Defenitino |
|-|-|
| Middleware | functions are functions that have access to the request object ( req ), the response object ( res ), and the next function in the application's request-response cycle |
| request object | allows you to submit a POST or GET request to an URL. Essentially it provides a way to make REST API requests to another URL |
| Response Object | It is the object which communicates between the server and the output which is sent to the client. |
| Route middleware | in Express is a way to do something before a request is processed. This could be things like checking if a user is authenticated, logging data for analytics, or anything else we'd like to do before we actually spit out information to our user. |