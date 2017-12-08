##Construction image docker
```  
cd 
docker build -t mysql .
```  

### Lancement container
```
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=norsysways -e MYSQL_USER=norsysways -e MYSQL_PASSWORD=norsysways -d mysql
```



### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

