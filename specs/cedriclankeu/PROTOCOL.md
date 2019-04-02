# Client-server protocol





## Phase 1: write the specification 

specification:

- What transport protocol do we use?

  ```
  TCP 
  ```

- How does the client find the server (addresses and ports)?

  ```
  127.0.0.1:8080    
  
  addresse is 127.0.0.1 and port is 8080
  ```

- Who speaks first?

  ```
  The client speak first while while the server is waiting for a request on it own side.
  ```

- What is the sequence of messages exchanged by the client and the server?

  ```
  The client will first of all ask for a connection request 
  
  The server will answer by connecting the client
  
  Then , the client will exchanged with the server by writing the todo maths operation , then reciproxly the server reply by sending the request answer.
  
  once the client close(EOF notification) the connection, the server is alerted and will then closed the communication.
  ```

- What happens when a message is received from the other party?

  ```
  Once the server receive the message, he will do the calculated the maths operation and send it 	back to the owner.
  
  The client will receive the answer the print it on the screen.
  ```

- What is the syntax of the messages? How we generate and parse them?

  ​	

  ```
  Client :  >1+1
  
  Server:   >1+1 = 2
  
  We parse them through command line. The messages exchanged  are strings.
  ```

- Who closes the connection and when?

  ```
  The client can closed the connection.
  
  Otherwise, the server can also closed it if after a lapse of time(1min) , there is no demande
  ```

- Submit a PR



## Phase 2: review 3 specifications 

- Are there big differences between the specification?

  ​		

  ```
  Of course , the are big differences between those specifications
  ```

- What are the common elements?

  ​		

  ```
  The point 3,4,5,7 seems similar
  ```

- Are there missing or confusing elements in the specification?

  ```
  No
  ```
