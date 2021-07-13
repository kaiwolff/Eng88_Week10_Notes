Setting up a token and passign it as part of the code is not recommended. Therefore, we will use postman to test API calls and tokens.

Postman is useful for testing responses to particular requests, and allows the user to look at the html of the pages that are being worked with.

Console shows extra details, rather than just the response body.

Can also add a token, via authorisation -> Bearer Token

Bearer tokens are sent in the ehader of the request, which is considered better practice than sending a token as part of the request body

Postman is useful for testing anything API related, or when a large number of URLs need testing

Requests can be saved to a workspace, and used to test a webapp, for example.


Thing to not e is that anyone with a token can extract the information if there is no encryption.  A token dsoes not provide confidentiality. For confidentiality, would need an SSL or TLS certificate, which would then allow authentication. The token can then be passed over a secure connection. By passing the token over a secure connection, it will not be plaintext and therefore more difficult to decode.

Difficult hting is to revoke tokens, as there is no official way to revoke tokens (outside of expiry dates). Workaround might be a deny list, against which incoming tokens are checked.


Instead of passing token in body, save it to lcal storage. for this, need javascript


use <script. in html, select javascript and write command ot store token locally

Now, we can use the getitem command to get the token back. An exampel code snippet is below:

```html
<script type="text/javascript">
windows.localstorage.setItem("myToken, "{{token}}")
var myToken = windows.localstorage.getItem("myToken)
alert(myToken)
</script>
```
notice that windows.localstorage is only used by windows


