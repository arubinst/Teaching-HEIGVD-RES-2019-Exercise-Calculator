### Specification : client-server communication

#1. What transport protocol do we use?

TCP

#2. How does the client find the server (addresses and ports)?

Localhost port 8000

#3. Who speaks first?

when the connection is established, the client will send a message

#4. What is the sequence of messages exchanged by the client and the server?

The client send a TCP packet containing an instruction to execute
The server compute the operation and respond the result

#5. What happens when a message is received from the other party?

The message will compute and a result is returned to the client

#6. What is the syntax of the messages? How we generate and parse them?

With a JSON document, create by the client and parsed by the server like :

{
  "operator":"+",
  "operand1":"2",
  "operand2":"3"
}

#7. Who closes the connection and when?

the server, when he returned the result.
