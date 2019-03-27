# What transport protocol do we use?
    For this purpose, I recommend using TCP
# How does the client find the server (addresses and ports)?
    By argument to the client / by config file
# Who speaks first?
    The client tries to contact the server then the server responds if available
# What is the sequence of messages exchanged by the client and the server?
    1) Client : Hello
    2) Server : Hello Client
    3) Client : could you compute ... ?
    4) Server : Doing that
    5) Client : Waiting
    6) Server : Here is your response
    7) Client : Got that
    8) Client : Either new operation or bye
    9) Server : if bye Bye or else start again at step 4) 
# What happens when a message is received from the other party?
    Logging it in the console would be a good solution
# What is the syntax of the messages? How we generate and parse them?
    Ex : _5Vs7q#...message...#3nd5Vs7q_
         _5Vs7q#    : start tag of message
        #3nd5Vs7q_  : end tag of message 
# Who closes the connection and when?
    The server if the client has disconneced wrongly or did not respond for x time.
    The client by sending bye (normal behaviour).
    
