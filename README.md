# Docker Apache Guacamole

Apache Guacamole is a clientless remote desktop gateway. It supports standard protocols like VNC, RDP, and SSH.

## Link
https://guacamole.apache.org/

## Deploy service 
Use docker-compose to start service

```
docker-compose up -d
```


## Open website:
```
http://IP:8080/guacamole/#/
```

**Username**:guacadmin  
**Password**: guacadmin  

## First login after deploy:

When access to that site: 
  ```
  http://IP:8080/guacamole/#/
  ```

![obraz](https://user-images.githubusercontent.com/86531003/233181710-b6773e0d-70fa-4b49-a6fb-910b1f5246e1.png)


Additional setup MYSQL need to be done:

* copy sql file to path 
```
cp 01-initdb.sql my-db/
```
* login to MySQL container  
```
docker exec -it da8993cb1b76 bash
```
* Login to root  
```
 mysql -u root -p
```
* use guacamole_db database  
```
use guacamole_db;
```
``` 
show databases;

```


* Execute file *sql  
```
source 01-initdb.sql
```

