# Protocol definition
### What transport protocol do we use?
We use TCP

### How does the client find the server (addresses and ports)?
The client use ip and port of the server.
- IP : 172.10.10.10
- PORT  : 6666 
### Who speaks first?
The client speaks first

### What is the sequence of messages exchanged by the client and the server?
1. The client send the formatted instruction to execute.
2. The server respond with the result or an error if the instruction is malform.

For exemple :
1. Client send : 12 * 2
2. Server respond : 24

### What happens when a message is received from the other party?
The message will be process and return to the client after calculation.

### What is the syntax of the messages? How we generate and parse them?
- the client send a literal string : "5 + 9"
- the server parse this string and operate the correct calculus
- the server send a literal string : "14"

### Who closes the connection and when?
The server close the connection after send the result