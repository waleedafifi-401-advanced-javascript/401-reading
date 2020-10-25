# OAuth

__Why is authentication important?__  
This is an important part of protecting a users info. If we do not use good authentication, then the wrong people could sign into other user accounts.

__Why should we be careful about storing a user’s password?__  
It is important becuase a user might have sensitive information that they are storing on the site or app. By asking for sensitive information, it is important to be responsible with the passwords to keep the users safe.  

__What is the difference between hashing and encryption?__  
Something that is encrypted can be decrypted. Something that is hashed cannot be unhashed, it is a one way function. Hashing is more secure than encryption.  
https://gcn.com/articles/2013/12/02/hashing-vs-encryption.aspx#:~:text=Encryption%20is%20a%20two%2Dway,to%20reveal%20the%20original%20password.

__What is the difference between encryption and encoding?__   
Encoding can be reversed by the same algorithm, but encryption needs a key to be reversed, so encryption is more secure than encoding.  
https://danielmiessler.com/study/encoding-encryption-hashing-obfuscation/#:~:text=Encoding%20is%20for%20maintaining%20data,order%20to%20return%20to%20plaintext.

__What is a token used for?__  
A token is used to authenticate a a user.  

## Vocabulary Terms  
  
|Term | Definition |  
|---|---| 
| authentication | Verifying a user's identity by requiring pre-required details. https://medium.com/@pavithraranathunga/the-most-common-authentication-methods-in-web-application-development-35845ecb1da0#:~:text=When%20it%20comes%20to,(Commonly%20username%20and%20password).|
| authorization | The process of allowing a user access to a resource. https://medium.com/@pavithraranathunga/the-most-common-authentication-methods-in-web-application-development-35845ecb1da0#:~:text=When%20it%20comes%20to,(Commonly%20username%20and%20password).|
| encryption | The translation of data to another form so that only a secret key or password can read it. https://digitalguardian.com/blog/what-data-encryption| 
| hashing | The conversion of one value to another. This is done to make data like passwords difficult to decipher. https://techterms.com/definition/hash#:~:text=A%20hash%20is%20a%20function,checksum%20generation%2C%20and%20data%20indexing.| 
| session | Interactions with a website that take place in a given time frame. https://support.google.com/analytics/answer/2731565?hl=en#:~:text=A%20session%20is%20a%20group,social%20interactions%2C%20and%20ecommerce%20transactions. | 
| cookie | A small amount of data that is stored by the web browser to so a website can remember information about you. https://techterms.com/definition/cookie#:~:text=A%20cookie%20is%20a%20small,information%20for%20a%20specific%20site. | 
| token | With token based authentication, the user state is stored on the client. The data is encrypted in a JWT. The server then validates the JWT. https://dev.to/thecodearcher/what-really-is-the-difference-between-session-and-token-based-authentication-2o39| 
| Basic Auth | An authentication built into HTTP , where the authorization header contains the word basic followed by a space and an encoded string of `username:password` https://swagger.io/docs/specification/authentication/basic-authentication/ |
| encoding | The process of converting one code of data to another. It goes from something a user can understand to something less clear. https://techterms.com/definition/encoding| 
| secret | This ia a secret that only the application and authorizaiton server know. It should be random enough that it can not be guessed. https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/|
| cryptography | Protecting information by transforming it into a format that can not be easily understood. https://techterms.com/definition/cryptography#:~:text=Cryptography%20is%20the%20science%20of,used%20to%20protect%20digital%20data.| 