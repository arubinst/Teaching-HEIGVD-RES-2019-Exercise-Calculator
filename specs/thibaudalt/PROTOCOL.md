# Specification : Exercise-Calculator

## 1. What transport protocol do we use?
We use TCP (Transmission Control Protocol).

## 2. How does the client find the server (addresses and ports)?
We use localhost on port 8080.

## 3. Who speaks first?
The client try to reach the server.

## 4. What is the sequence of messages exchanged by the client and the server?
a) The client send a TCP packet containing an operation
b) The server compute the operation and send the result to the client

## 5. What happens when a message is received from the other party?
If the request is legitimate, it's examined. Otherwise it is ignored.

## 6. What is the syntax of the messages? How we generate and parse them?
A proposed syntax : "OPERATION;VARIABLES"
The client generates messages with some user input, the server parses the received TCP packets.

## 7. Who closes the connection and when?
The server close the connection when the client receive the operation result.
