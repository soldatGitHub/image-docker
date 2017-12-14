### Construction image docker
```  
docker build -t <nom-image> . 
```  
Exemple si on veut nommer l'image **mysql** : 
> docker build -t **mysql** .


### Lancement container
> Syntaxe : 
```
docker run -p <port-externe>:3306 --name <nom-container> \
	   -e MYSQL_ROOT_PASSWORD=<mdp-root>             \
           -e MYSQL_DATABASE=<nom-bdd>                   \
           -e MYSQL_USER=<login>                         \
           -e MYSQL_PASSWORD=<mdp>                       \
           -d <nom-image>                                \
```
Exemple : 
> docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=norsysways -e MYSQL_USER=norsysways -e MYSQL_PASSWORD=norsysways -d mysql



### Rentrer dans le container
```
docker exec -it <nom-container> bash
```
> docker exec -it **mysql** bash


