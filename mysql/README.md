### Construction image docker
```  
docker build -t <nom-image> . 
```  
Exemple :
Si on veut nommer l'image **mysql** : 
> docker build -t **mysql** .


### Lancement container
Syntaxe : 
```
docker run -p <port-externe>:3306 --name <nom-container> \
	   -e MYSQL_ROOT_PASSWORD=<mdp-root>             \
           -e MYSQL_DATABASE=<nom-bdd>                   \
           -e MYSQL_USER=<login>                         \
           -e MYSQL_PASSWORD=<mdp>                       \
           -d <nom-image>                                \
```
Exemple : 
```
docker run -p 3306:3306 --name mysql               \
	   -e MYSQL_ROOT_PASSWORD=root             \
           -e MYSQL_DATABASE=mydatabase            \
           -e MYSQL_USER=myuser                    \
           -e MYSQL_PASSWORD=mypassword            \
       
```
> url de connexion : jdbc:mysql://localhost:3306/mydatabase

### Lancement depuis docker-compose
```
docker-compose up -d --build 
```

### Rentrer dans le container
```
docker exec -it <nom-container> bash
```
> docker exec -it **mysql** bash


