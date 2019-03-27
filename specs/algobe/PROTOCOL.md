# PROTOCOLE

## What transport protocol do we use?
The client and the server use TCP to communicate with eachothers.

## How does the client find the server (addresses and ports)?
The client find the server with its IP address and using the port 2357.

## Who speaks first?
The client speaks first.

## What is the sequence of messages exchanged by the client and the server?
* The client asks to establish a connection.
* The server answers if the connection is accepted.
* The client sends a maths operation.
* The server sends the answer back.
* Repeat last 2 points as much as wanted.
* The client received enough knowledge for today and sends a disconnect operation
* The server sends it the disconnection is accepted.

## What happens when a message is received from the other party?
* The server does the operations and send them back.
* The client displays the answer received.

## What is the syntax of the messages? How we generate and parse them?
* The client sends the operation in a string, preceded by CAL: 
** Ex: CAL: 3 + 4
* The server receives the string and parses it, and send the answer back, preceded by ANS:
** EX: ANS: 7

## Who closes the connection and when?
* If something wrong happens, the server closes it.
* Otherwise the client asks to disconnect.

## Submit a PR
Ok I submit.
