1. What transport protocol do we use?
Nous utilsons le protocole TCP

2. How does the client find the server (addresses and ports)?
On passe en argument du client l'adrese et le port du serveur 

3. Who speaks first?
Le client parle en premier. 

4. What is the sequence of messages exchanged by the client and the server?
Client : ouvre le socket de connexion
Serveur : établit la socket de connexion
Client : communication (on utlise les flux d’entrées et sorties pour envoyer des équations et recevoir les resultats du serveur)
Serveur : traitement des équations en provenance du client (Du côté du serveur, nous ouvrons aussi les entrées inputStream et outputStream. Après avoir reçu l'équation, nous la traitons et renvoyons le résultat au client en écrivant sur le outputStream du socket.)
Client : ferme la connexion
Serveur : ferme la connexion

5. What happens when a message is received from the other party?
Le serveur décode les messages entrants et exécute la demande en appelant une routine (dispatching) qui gère la demande 
Le client code et envoie la demande au serveur. La réponse du serveur est ensuite transmise à l'utilisateur.

6. What is the syntax of the messages? How we generate and parse them?
Le message est une chaîne. Cette dernière contient les oprandes 1 et 2 et les opérations à éféctuer.
nous allons diviser l’équation en opérande et opération afn d'éffectuer le calcul.

7. Who closes the connection and when?
Le serveur ferme la connexion lorsqu'il a attendu un certain temps sans réponse ou lorsque le client a annoncé la fin de l'échange.


