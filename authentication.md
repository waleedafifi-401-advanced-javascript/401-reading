![](https://www.loginradius.com/blog/wp-content/uploads/sites/4/2019/10/Passwordless-Authentication-main-image-1024x576.png)

# Authentication

### User Modeling
***
- Modern day web use entails apps needing to store lots of sensitive info about users
  - Developer's responsiblity to do this!
- Passwords should be encrypted using hashing algorithm *before* its stored
  - This means even developers with db permissions can't access passwords
- User models that have sensitive data that should **NEVER** be sent to client applications

### Cryptography
***
- Science which studies methods for encoding messages so they can be read only by person with key (and hence the person who knows the secret information required for decoding)
- Cryptanalysis is the science of decoding encrypted messages without having the key (a lot under this umbrella term)

### Hash Algorithms
***
- **Cryptographic Hash Algorithm** takes data and produces has that is purposefully hard to reverse
  - Identical data produces same hash
  - Hash algos often used for checking integrity of data
- Example use in a User model:
  - Hash password stored when user signs up
  - When user logs in, resend their password and server hashes login pwd using same hash algorithm (because it's identical data)
  - Server compares hased login pwd with previously stored hased pwd to determine if user is good to go (can be authenticated)

### Cypher Algorithms
***
- **Cryptographic Cypher Algorithm** takes data and key and produces encrypted data
  - Can later be reversed into orig data by decrypting with same key
- **tokenSeed** is the random unique string that's used to make user token
  - Associate tokenSeed with user account, encrypt tokenSeed with a secret key only server knows
  - Send encrypted key back to user, now their **user token**
  - Client makes future request with that toke, server knows the secret key and can decrypt it
  - *tokenSeed unique to the database and can be queried to produce user who made request*

### Basic Authorization
***
- Common method for sending username and pwd in HTTP request
  - Username and pwd joined with **:** and then **base64 encoded** and placed after string **Basic**
  - **base64: character set that is safe to use**
    - azAZ09+.  (or maybe its = instead of +?)
      - a through z lower and upper, 0 through 9, + and . are the 64 characters
      - "make it work with these!"
  - Resulting full string set to value of Authorization header
  - Server can decode Basic Auth header to get username and pwd
  - Server usually responds to client with validation response (token or key)
- base64 is **not** encryption, client and server have to use **HTTPS** to protect username and pwd info
  - 256bit AES encryption is the standard at the moment for HTTPS
  - "over the wire"

- **Node app**: use node module since methods not built in
```
    let base64 = require('base-64');

    let string = 'someusername:P@55w0rD!';
    let encoded = base64.encode(string); // c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==
    let decoded = base64.decode(encoded); // someusername:P@55w0rD!
    Additional Resources
```

- **Browsers**: `atob` and `btoa` to convert to/from base64 encoding
```
    let encoded = window.btoa('someusername:P@55w0rD!')
    // c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==

    let decoded = window.atob('c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==');
    // someusername:P@55w0rD!

    request({
      method: 'GET',
      url: 'https://api.example.com/login',
      headers: {
        Authorization: `Basic ${encoded}`,
      },
    })
    .then(handleLogin)
    .catch(handleLoginError)
```

**what a “Singleton” is?**

A **singleton** is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object
