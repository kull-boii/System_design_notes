What is a Stateful Protocol? A Stateful Protocol is a type of network protocol in which the client sends a server request and expects some sort of response. In case it doesn't get a response, it then resends the intended request. A few examples of Stateful Protocol are Telnet, File Transfer Protocol (FTP), etc

A stateless protocol is a communication protocol in which the receiver must not retain session state from previous requests. The sender transfers relevant session state to the receiver in such a way that every request can be understood in isolation, that is without reference to session state from previous requests retained by the receiver

An HTTP server can understand each request in isolation.

Contrast this with a traditional FTP server that conducts an interactive session with the user. During the session, a user is provided a means to be authenticated and set various variables (working directory, transfer mode), all stored on the server as part of the session state.

if you can restart your server and your clients can still communicate then your protocol is stateless.

### why tcp is stateful:
https://youtube.com/shorts/n-paFbO1hXE?feature=share

## References:
- https://en.wikipedia.org/wiki/Stateless_protocol
- https://www.youtube.com/watch?v=OAx7Z99pFyQ
- https://byjus.com/gate/difference-between-stateless-and-stateful-protocol/
