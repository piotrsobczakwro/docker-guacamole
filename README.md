# docker-guacamole

## Deploy service 

```
# docker-compose up -d
```


## Open website:
http://<IP>:8080/guacamole/#/


**Username**:guacadmin; 
**Password**: guacadmin

## First login after deploy:

When access to that site: 
  ```http://<IP>:8080/guacamole/#/```

![obraz](https://user-images.githubusercontent.com/86531003/233181710-b6773e0d-70fa-4b49-a6fb-910b1f5246e1.png)

Solution:
 

cp 01-initdb.sql my-db/
docker exec -it da8993cb1b76 bash


 mysql -u root -p
 
 mysql> use guacamole_db
Database changed
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| guacamole_db       |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.00 sec)

mysql> source 01-initdb.sql


mysql> source 01-initdb.sql
Query OK, 0 rows affected, 5 warnings (0.12 sec)

Query OK, 0 rows affected, 6 warnings (0.07 sec)

Query OK, 0 rows affected, 2 warnings (0.04 sec)

Query OK, 0 rows affected, 3 warnings (0.05 sec)
