Instead of making user authenticate each step, send something to authenticate each requerst,and re-use this. 2 main types:

- Token-based
- Cookie-based

Note token-based is different from physical token used fo rauthetnication in multi-factor authentication.


### Cookie-based

Sejnd a cookie (a small piece of data) to browser

Browsers store and send cookie back to the server to authenticate that a request is coming from the same browser, keeping the user authenticated. Browser cookies are read as key-value pairs.

Typical chain of events:

Client sends login request wiht credentials. Validated by server or backened. Create a session. Will include a header in the response with a "set cookie" option, where a session ID is established. Cookie is saved by browser. Cookie used to verify session until logout request from browser deletes the session on the server

Cookies cause the app itself to become stateful. This has the disadvantage that a browser is bound to a particular server runnign that particular app.
Cookies are small in size, this means not a lot of information regarding the session can be stored client-side. Conversely, the app becoming stateful can be an advantage for tracking and personalising an app for a user (e.g. the classic advertising cookies). Another advantage is that it can be automatically added to a request, meaning not a lot has to be done by a user, though some extra processing has to be done server-side;.

Cookies work on a single domain only. 


### Token-based authentication

Token used to store the user's state on the client machine.

JSON web Token (JWT) is open standard that defines a way of securely transmitting info between client and a server as a json object.

Anatomy: three parts separated by dots

3 parts are JWT header, JWT payload, JWT signature

JWT header is a base64 encoded JSON object.
Payload contains some information about the user account

Signature: HMAC-SHA256(base64UrlEncode(header)+"."+base64UrlEncode(paylod),secret).

### Token-based step-by step:

Login request by client, authenticated server-side. Instead of generating a session, the server generates a toke and sends it back to the client. Client saves token, and uses it to make requests. The server verifies whether the token is valid or not. Token is valid until expiry or logout, after which the token is deleted.


Advantage: app is back to being stateless because the session does not need to be verified, only that hte token holds the correct information. 

Limitations: Token is bigger than cookie, depending on the amount of information contained in the payload. This can slow down the request itself as the token will be added to all of the requests.

#### Comparison

Cookies: client-side files. Ends depending on lifetime. Maximum filesize of 4kb.

Token: only token at client-side. Can contain as much data as is necessary, unlike cookie. 


When to use cookie, and when to use session: When you want the user profile to be known and have personalisation (either for the user's benefit or to track things such as purchases), cookies are a good choice


When an app needs to be used on different platforms, including for example items without browser (IoT devices and such), a token is a better choice.



