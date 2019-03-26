# Teaching-HEIGVD-RES-2019-Exercise-Calculator
The first goal is to **specify a client-server protocol**, which will allow a client to ask a server compute a calculation and to return the result. 

The specification must contain everything that is needed for **one person to implement a client**, for **another person to implement a server** and for the 2 applications to work together. The specification is a contract between the server and the client.

## Phase 1: write the specification (15 minutes)

* Fork this repo and **create a folder with your GitHub ID in the "specs" folder**
* In this folder, create a file named `PROTOCOL.md` and write your specification:
  * What transport protocol do we use?
  * How does the client find the server (addresses and ports)?
  * Who speaks first?
  * What is the sequence of messages exchanged by the client and the server?
  * What happens when a message is received from the other party?
  * What is the syntax of the messages? How we generate and parse them?
  * Who closes the connection and when?
  * Submit a PR
* **Open a PR**

## Phase 2: review 3 specifications (15 minutes)

- Are there big differences between the specification?
- What are the common elements?
- Are there missing or confusing elements in the specification?

## Phase 3: validate specs in pairs (15 minutes)

* Work with the student sitting next to you
* One of them is the server, the other is the client
* Pick one of the 2 specifications
* One student uses netcat (nc) to start a server (nc -kl). The other student uses netcat to start a client.
* Go through a couple of scenarios to validate that your specification is complete (if you need to ask something to the other student, or if you need to discuss, you probably should make your specification more complete)

## Phase 4: implement a client a server (45 minutes)

- One student implements a client in Java
- The other student implements a server in Java
- The team performs various tests to validate that the client and the server work together (on the same machine, across two machines connected to the same network, in Docker containers)



