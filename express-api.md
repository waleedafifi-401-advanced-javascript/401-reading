![](https://cdn.fuga.cloud/fuga-assets/dist/images/articles/api-example.jpg)
# API Server

#### Router Parameters
* When you get params on a route (`:paramName`) you can access it with `req.params.paramName`
* You can call middleware like this `app.get('/places/:city', middleWareCall, (req,res) => {})`, or `app.use`
* `router.param` lets you run middleware only when certain params are present

#### Sub Documents in Mongoose
* Mongoose gives structure to Mongo documents. NoSQL databases are not structured by default
* You can define sub documents in a Mongoose schema to help do more with your data
* This may be difficult to keep track of, but it has some benefits when organizing data

#### Joining Data/Documents in Mongo
* `populate()` is a method for joining 2 collenctions
* You can also make a virtual field in a document that points to another.
* With `pre('find')` you can do a collection on the fly rather than storing the relation
* You can also create a reference column that has all the `_id`s of the document to make quicker `finds()`

#### Middleware
**Middleware** (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins. Mongoose 4.0 has 2 types of middleware: document middleware and query middleware.

#### Terms
| Terms | Defenition |
|-|-|
| Routing | refers to how an application’s endpoints (URIs) respond to client requests. |
| Route Prefixing | Route grouping is a concept to make the route function that receive same prefix of different requests |
| Request `Body` | data sent by the client to your API |
| Request `Query` | QueryString is a collection used to retrieve the variable values in the HTTP query string |
| Request `Params` | combination of the keys/values you’ll find in `Request.Querystring` , `Request.Form` , `Request.Cookies` , `Request.ServerVariables` |