![](https://www.ionos.com/digitalguide/fileadmin/DigitalGuide/Teaser/was-ist-http-t.jpg)

# HTTP and REST

* HTTP stands for HyperText Transfer Protocol
* HTTP defines how requests and responses should be formatted between clients and servers. It is the foundation of the world wide web
* The first line of an HTTP request contains the __METHOD__, __URL__, and __HTTP VERSION__. These are followed by the __HEADERS__, which are key value pairs. 
* __Safe__ methods are for retrieval, __Idempotent__ methods will always get the same response, and __Cacheable__ means the client should be able to cache the response
* The HTTP response contains the __HTTP VERSION__, __STATUS CODE__, and the __STATUS MESSAGE__ on the first line and the request headers on the second line. 
* __REST__ stands for REpresentational State Transfer.
* RESTful endpoints deliver data in JSON formanta
* REST APIs are documented with a a "live" documentation known as Swagger, which show you how to use an API and give you the ability to make live requests from it
* Swagger allows you to create your own documentation for your API.

### The HTTP operations available are
* POST (create a resource or generally provide data)
* GET (retrieve an index of resources or an individual resource)
* PUT (create or replace a resource)
* PATCH (update/modify a resource)
DELETE (remove a resource)


![](https://www.univention.com/wp-content/uploads/2020/04/200416-rest-api.jpg)

### What Is A REST API

* API stands for application program interface, consisting of a structeured request and response
* REST is an architecture style for desigining network applications and relies on HTTP
* PUT is used generally in web forms
* PUT updates a resource
* Rarely used requests are __HEAD__, __OPTIONS__, and __PATCH__
* An endpoint is the URI/URL where the api is accessed by a client
* Postman is used to make API requests


### Terms
| Term | Definition |
|-|-|
|**lifecycle** | is a project management model that defines the stages involved in bringing a project from inception to completion |
|**collections** | is a form of memory management whereby objects that are no longer referenced are automatically deleted and their resources are reclaimed. |
|**the “Repository” design pattern** | Repository pattern is a kind of container where data access logic is stored. It hides the details of data access logic from business logic. |
|**mongoose middleware** | Document middleware is supported for the following document functions. In document middleware functions, this refers to the document.|
|**Object Relation Mapping (ORM)** | ORM, O/RM, and O/R mapping tool) in computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages |


##### Cloud based NoSQL Databases
1. Amazon DynamoDB.
1. Amazon SimpleDB.
1. Azure Cosmos DB.
1. Cloudant Data Layer (CouchDB)
1. EnterpriseDB Postgres Plus Cloud Database.
1. Google Cloud Bigtable.
1. Google Cloud Datastore.
1. MongoDB Database as a Service (several options)

