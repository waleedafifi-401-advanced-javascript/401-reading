## RaBAC
In computer systems security, role-based access control (RBAC) or role-based security is an approach to restricting system access to authorized users. It is used by the majority of enterprises with more than 500 employees and can implement mandatory access control (MAC) or discretionary access control (DAC).

 
## Access Control (ACL)
Access Controls are the selective restriction of resources. Access Controls are implemented everywhere in computer systems. UNIX files have read, write, and execute permissions assigned to owners, groups, and everyone else. Websites have limited access to pages based on the credentials of a user. APIs restrict access to internal and external developers differently.

**In our RESTful APIs**, it is important to limit access to clients based on credentials. This means a user (Foo) should not be able to delete a users (Bar) resource, unless Bar said that Foo is allowed to. Limiting what actions a user can preform on a given resource is called Access Control. A user can be given a token at signup and login, and that user can pass that token back to the server on requests with limited access controls. Once the server parses the token, it can determine if the user is authorized to preform the request.

**Application Flow and Access Control**

Applications of all types have varying degrees of access based on user type and UI requirements.

**A CMS might**

- Allow admin users to create categories, content, manage user accounts, and run reports
- Allow editor users to create, edit and delete existing content, but not see or manage user accounts
- Allow guest users to access (read) content
- Allow user users (logged in users) to access (read) content and apply a thumbs-up/down to content, but not change the actual content
- Each of these constraints will have to be handled on both the backend and the front end of your application stack.

- Back End (API Layer)
- Manage the login cycle with the front-end application
- Maintain the User’s database
- Maintain roles for each user
- Authenticate users (basic and bearer)
- Create, manage, and apply Role Based Access Controls
- Maintain and reference their capabilities, based on their role
- Restrict access to features (like routes) based on capabilities
- Express Middleware could be used to restrict access to routes
- Mongoose Middleware/Hooks could be use to restrict access to business logic

- Front End (Client Layer)
- Initiate the login process
- Store login tokens as cookies
- Manage login state, capabilities
- Control physical & visual access (hide/show/alter) to components based on RBAC rules
- Alter behaviors based on RBAC rules

__When is Basic Authorization used vs. Bearer Authorization?__
 Basic authorization is the simplest version of authorization and the least secure. It may be used for a read only resource, and it should only be used with HTTPS because the encryption can be easily reversed. Bearer authoriztion uses a token and is more secure for an exchange between a client and a server.  

__What does the JSON Web Token package do?__  
It defines packages for securely transmitting information as a JSON object. It is can be signed with a secret, whcih certifies that the only owner of the secret is the party the signed the JWT.  

__What considerations should we make when creating and storing a SECRET?__  
It is best to make a secret that is random and unguessable. It should be stored in the .env file, though there may be some better options. The goal with a secret is to make sure nobody has access to it, to keep your app secure.  


|Term | Definition |  
|---|---| 
| encryption | The method by which information is converted into a secret code that protects the data from being easily understood. https://searchsecurity.techtarget.com/definition/encryption |
| token | These are strings or JWTs that let an api know that the token bearer is authorized. https://www.oclc.org/developer/develop/authentication/access-tokens.en.html |
| bearer | The bearer is the 'owner' of the token in bearer authentication. The bearer shows the token and is granted access to the resource or URL. https://blog.restcase.com/4-most-used-rest-api-authentication-methods/|
| secret | This is often sent along with a client id to a resource to obtain a token. It is only known to the OAuth Client and the authorization server. https://developers.google.com/youtube/registering_an_application|
| JSON Web Token | A method for securely transmitting JSON objects between different parties. The tokens can be transmitted as query strings, header attributes, or in the body of a POST request. JWT is popular because of teh small size. https://auth0.com/learn/token-based-authentication-made-easy/ |
