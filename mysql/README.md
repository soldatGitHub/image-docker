### Construction image docker
```  
docker build -t <nom-image> . 
```  
Exemple : 
> docker build -t **mysql** .


### Lancement container
```
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=norsysways -e MYSQL_USER=norsysways -e MYSQL_PASSWORD=norsysways -d mysql
```
Exemple : 
> docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=norsysways -e MYSQL_USER=norsysways -e MYSQL_PASSWORD=norsysways -d mysql



### Rentrer dans le container
```
docker exec -it <nom-container> bash
```
> docker exec -it **mysql** bash


