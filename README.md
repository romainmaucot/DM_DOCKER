DM_DOCKER

Vous souhaitez automatiser la création et la configuration d'un environnement de développement autonome que chaque développeur peut utiliser sur sa machine.(docker compose) 
L'objectif est que tous les développeurs puissent travailler sur un environnement totalement identique.
 Pour cela, vous avez décidé d'utiliser Docker.

Vous devez fournir une solution technique avec Docker permettant à tous les développeurs d'installer rapidement votre application.
 Celle-ci doit tourner avec :

Apache / PHP 7.2 avec l'extension pdo_mysql 
(avec une commande créée par docker, renseignez vous dans la documentation), sur le port 30000
Mariadb
Adminer sur le port 50000
Vous devez ajouter un utilisateur à l'image, et ajouter cet utilisateur au groupe faisant tourner le serveur apache. Utiliser des commandes linux pour chercher et remplacer des chaines de caractère dans le fichier de configuration apache de sorte à changer le DocumentRoot de l'image Docker.

Vous devez utiliser les Dockerfiles et Docker-Compose pour qu'il soit possible en une commande de créer l'environnement pour lancer l'application.
