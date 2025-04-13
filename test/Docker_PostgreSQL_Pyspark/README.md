Hiérarchie des dossiers 

Devoir_NBA-n_3/
├── data/                        # Données brutes ou nettoyées
├── documentation/              # Docs techniques, rapports, etc.
├── notebook/                   # Notebooks Jupyter (.ipynb)
├── test/                       # Scripts de test                   
│   └── Docker_PostgreSQL_Pyspark/
│       └── docker-compose.yml  # Fichier de configuration des conteneurs
          etc
├── utils/    



Vérifier si Docker est bien installé
````bash
docker --version
````

Vérifier si la version de Docker compose est installé 
````bash 
docker compose --version
````

Démarrer le conteneur
````bash
docker-compose up -d
````

Afficher les conteneurs 
````bash
docker ps 
````

Si tout fonctionne bien normalement, il doit avoir 2 images, un PostgreSQL et Pyspark avec jupyther

````bash
docker logs spark-nba
````

Normalement tu veras dans la commande 

````
http://127.0.0.1:8888/?token=abcdef123456...
````

&rarr; Copie le lien complet et colle-le dans ton navigateur pour ouvrir Jupyter.

Vous retrouvez un fichier *test.ipynb* avec du code pyspark et *play_by_play.csv* 

Pour apprendre Pyspark aller sur SSPcloud ou vidéo Youtube 

Pour voir si l'image PostgreSQL
````bash
docker exec -it postgres-nba psql -U nba -d nba
````

Arrêter un conteneur actif

````bash
docker stop nom_du_conteneur
````
Test
