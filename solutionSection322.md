Anis Drissi equipe 7

### La solution de a question 3.2 est :
Sauvegarder un fichier index.html sur notre machine

Ouvrir une console et se placer dans le répertoire où se trouve le fichier

Si le conteneur httpd n'est pas lancé, l'éxecuter avec la commande docker run --name httpd-soluce -d -p 8080:80 httpd (8080 est le port que l'on affecte au port du conteneur)

On peut utiliser la commande "docker ps" pour voir l'identifiant du conteneur
CONTAINER ID   IMAGE     COMMAND              CREATED          STATUS          PORTS                  NAMES
134c4e56074e   httpd     "httpd-foreground"   42 minutes ago   Up 42 minutes   0.0.0.0:8080->80/tcp   httpd-User435arch

Pour copier le fichier index.html, lancer la commande "docker cp ./index.html <CONTAINER ID>:/usr/local/apache2/htdocs/index.html
remplacer CONTAINER ID par l'identifiant récupéré

Si on écrit localhost:8080 sur notre navigateur, le message s'affiche sur la page :
"Le fichier index.html a été modifié"