# Authentication and Authorization using JWTs in Node.js

The objective of this project is to implement the concept of access token and refresh token mentioned in the OAuth2.0 specification (RFC 6749). We’ll use JSON Web Tokens (JWT) for this purpose.

## Project outline

In this project, we’ll create two server applications viz. authentication cum authorization server and resource server. The functions of both the servers are described below.
(i) Authentication cum authorization server — This server will register new users and will enable them to log-in. On successful log-in, it will provide the users with access and refresh tokens, with the help of which the users will be able to access the resource. It will also generate new access tokens once it receives correct refresh token from the user. If the access token gets compromised/stolen from the user, then it will also have the ability to delete the refresh token from the database once the user requests for it. And it will not generate any more access tokens for the user.
(ii) Resource server — This server will verify the access token received from the user and on successful verification, it will allow the user to access the resource.
The users will be able to access all the endpoints using cURL from the terminal.
