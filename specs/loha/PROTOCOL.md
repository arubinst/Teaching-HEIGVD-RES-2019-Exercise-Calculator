What transport protocol do we use?
TCP
How does the client find the server (addresses and ports)?
La première chose est de définir un numero de port sur lequel le service, côté serveur, tournera ex : 9090.
L'adresse du serveur doit être connu par le client. Le serveur n'a pas besoin de connaître initialement l'adresse du client.
Who speaks first?
La première personne à initier la conversation est le client en utilisant l'adresse et le port du serveur. Et demande au serveur s'il est disponible. S'il n'a pas de réponse, il ressaie toutes les 30 secondes.
What is the sequence of messages exchanged by the client and the server?
Le serveur enregistre l'adresse du client et luit répond "SURICATE" pour signifier qu'il est en écoute et lui transmet un ID unique que le client doit utiliser a chaque fois qu'il veut parler au serveur
What happens when a message is received from the other party?
Le serveur va vérifier que le message contient des phrases compréhensibles et qu'il est autorisé à effectuer. Il exécute la commande et renvoie la réponse au client.
What is the syntax of the messages? How we generate and parse them?
On envoie son ID, le mot CMD suivit de du nom de commande ensuite les arguments
Who closes the connection and when?
Le client ou le serveur. Soit s'il n'y a plus de réponse depuis un certain délais, sois il ya trop de communication échouée. le mot close connection est envoyé par le client ou le serveur.
