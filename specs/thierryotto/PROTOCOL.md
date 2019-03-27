Spécifications "Exercise-Calculator"

1) What transport protocol do we use?
TCP

2) How does the client find the server (addresses and ports)?
L'adresse IP et le port doivent être prédéfinis en statiques et à l'avance

3) Who speaks first?
Le client indique au serveur qu'il veut exécuter des requêtes de calcul, donc le client parle en premier.

4) What is the sequence of messages exchanged by the client and the server?
	a. Le client s'annonce au serveur et attend sa confirmation
	b. Le serveur confirme au client qu'il peut accepter des requêtes et se met en attente d'une requête
	c. Le client envoi une requête de calcul au serveur
	d. Le serveur reçoit la requête, traite le calcul et retourne le résultat au client
	e. Recommencer autant de fois que nécessaire les points c et d
	f. Le client indique au serveur qu'il a fini
	g. Le serveur termine la connexion

5) What happens when a message is received from the other party?
	Si la requête est légitime le serveur traite la requête, sinon il l'ignore.

6) What is the syntax of the messages? How we generate and parse them?
	a. Annonce : "Hello"
	b. Confirmation : "confirm"
	c. Requête de calcul : "operation:opérande1:opérande2"
	d. Résultat : "result:xxx"
	e. Fin de la connexion : "end"

7) Who closes the connection and when?
Le client indique au serveur qu'il n'a plus de requête, le serveur termine la connexion.
