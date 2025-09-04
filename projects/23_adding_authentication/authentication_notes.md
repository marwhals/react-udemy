# React authentication notes

---

## How does authentication work

- Client request *with user credentials*
- Any client can send a request that tells the backend that we were previously granted access

### Two options to implement this

- Server-side Sessions
  - Store unique identifier on server, send same identifier to client
  - Client sends identifier along with requests to protected resources
  - Server can check if the identifier is valid i.e previous issue by the server to the client
    - Causes tight coupling
  - Most react apps are SPAs that are server by a server that is decoupled from the backend
  - The SPA handles routing (on the client side) and only "talks" to the backend if it needs data (or needs to change data)
    - A backend can server multiple apps etc
- Authentication Tokens
  - Create (but not store) "permission" token on server and send it to the client
  - Client attaches token to future requests for protected resources
  - Server can then verify the attached token