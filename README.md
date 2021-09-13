# My SQL 

## Login

```
mysql -uroot -p
```

it asks for password, provide password and enter


----

# Dockerized Container for Mysql

## Pull the latest mysql server
```
docker pull mysql/mysql-server:latest
```

Docker images to view inmages in the system




## Run the image

Customizable - port number, name


```
docker run -p 3306:3306 -d --name=mysql mysql/mysql-server:latest
```


## List running containers 
```docker ps```

See the logs of mysql
Docker logs mysql

It will have generated root password, copy it some where safe


Execute docker insider mysql
Docker exec -it mysql bash


Inside mysql bbash type login details
Mysql -uroot -p

It asks for password
Give the password

Until now we logged into the linux container that contains mysql

Now lets interact wit mysql app


It logs into mysql app


-------------
My Sql Password
-------------
e7#E342JTN?=aU7.6LbJtJ#oe8^7a=k_
---------------


Change this root user password

ALTER USER 'root'@'localhost' IDENTIFIED BY 'new password'

Exit mysql
 Type backward slash and alphabet q
\q


----

# LOGS

Last login: Tue Sep  7 12:51:15 on ttys001
LM-SJC-11009966:~ pmalyalavenkatad$ docker pull mysql/mysql-server:latest
latest: Pulling from mysql/mysql-server
8969f19fb2cc: Pull complete 
18ff34a960f0: Pull complete 
1059844cbb8f: Pull complete 
3bd4cb0b78d1: Pull complete 
901b41fa66ef: Pull complete 
b33be9f4a1f3: Pull complete 
38b3da6a86f7: Pull complete 
Digest: sha256:5241f7de0483a70f5856da995fea98904cfce8f1c51734b7f3836c1663eead17
Status: Downloaded newer image for mysql/mysql-server:latest
docker.io/mysql/mysql-server:latest
LM-SJC-11009966:~ pmalyalavenkatad$ docker run -p 3307:3307 -dd --name=mysql mysql/mysql-server:latest
f9f64853cdf965680be29ba77029566d157677462b1bb7a8a3eead1971542b9f
LM-SJC-11009966:~ pmalyalavenkatad$ docker ps
CONTAINER ID   IMAGE                       COMMAND                  CREATED         STATUS                            PORTS                                                                  NAMES
f9f64853cdf9   mysql/mysql-server:latest   "/entrypoint.sh mysq…"   4 seconds ago   Up 2 seconds (health: starting)   3306/tcp, 33060-33061/tcp, 0.0.0.0:3307->3307/tcp, :::3307->3307/tcp   mysql
LM-SJC-11009966:~ pmalyalavenkatad$ docker logs mysql
[Entrypoint] MySQL Docker Image 8.0.26-1.2.4-server
[Entrypoint] Initializing database
[Entrypoint] No password option specified for new database.
[Entrypoint]   A random onetime password will be generated.
2021-09-13T05:58:25.338293Z 0 [System] [MY-013169] [Server] /usr/sbin/mysqld (mysqld 8.0.26) initializing of server in progress as process 18
2021-09-13T05:58:25.369120Z 1 [System] [MY-013576] [InnoDB] InnoDB initialization has started.
2021-09-13T05:58:26.024849Z 1 [System] [MY-013577] [InnoDB] InnoDB initialization has ended.
2021-09-13T05:58:26.987283Z 0 [Warning] [MY-013746] [Server] A deprecated TLS version TLSv1 is enabled for channel mysql_main
2021-09-13T05:58:26.987783Z 0 [Warning] [MY-013746] [Server] A deprecated TLS version TLSv1.1 is enabled for channel mysql_main
2021-09-13T05:58:27.085158Z 6 [Warning] [MY-010453] [Server] root@localhost is created with an empty password ! Please consider switching off the --initialize-insecure option.
[Entrypoint] Database initialized
2021-09-13T05:58:30.689508Z 0 [System] [MY-010116] [Server] /usr/sbin/mysqld (mysqld 8.0.26) starting as process 65
2021-09-13T05:58:30.714329Z 1 [System] [MY-013576] [InnoDB] InnoDB initialization has started.
2021-09-13T05:58:30.930957Z 1 [System] [MY-013577] [InnoDB] InnoDB initialization has ended.
2021-09-13T05:58:31.171635Z 0 [Warning] [MY-013746] [Server] A deprecated TLS version TLSv1 is enabled for channel mysql_main
2021-09-13T05:58:31.171827Z 0 [Warning] [MY-013746] [Server] A deprecated TLS version TLSv1.1 is enabled for channel mysql_main
2021-09-13T05:58:31.173786Z 0 [Warning] [MY-010068] [Server] CA certificate ca.pem is self signed.
2021-09-13T05:58:31.174010Z 0 [System] [MY-013602] [Server] Channel mysql_main configured to support TLS. Encrypted connections are now supported for this channel.
2021-09-13T05:58:31.196029Z 0 [System] [MY-011323] [Server] X Plugin ready for connections. Socket: /var/run/mysqld/mysqlx.sock
2021-09-13T05:58:31.196044Z 0 [System] [MY-010931] [Server] /usr/sbin/mysqld: ready for connections. Version: '8.0.26'  socket: '/var/lib/mysql/mysql.sock'  port: 0  MySQL Community Server - GPL.
Warning: Unable to load '/usr/share/zoneinfo/iso3166.tab' as time zone. Skipping it.
Warning: Unable to load '/usr/share/zoneinfo/leapseconds' as time zone. Skipping it.
Warning: Unable to load '/usr/share/zoneinfo/tzdata.zi' as time zone. Skipping it.
Warning: Unable to load '/usr/share/zoneinfo/zone.tab' as time zone. Skipping it.
Warning: Unable to load '/usr/share/zoneinfo/zone1970.tab' as time zone. Skipping it.
[Entrypoint] GENERATED ROOT PASSWORD: e7#E342JTN?=aU7.6LbJtJ#oe8^7a=k_

[Entrypoint] ignoring /docker-entrypoint-initdb.d/*

2021-09-13T05:58:33.775645Z 11 [System] [MY-013172] [Server] Received SHUTDOWN from user root. Shutting down mysqld (Version: 8.0.26).
2021-09-13T05:58:34.885996Z 0 [System] [MY-010910] [Server] /usr/sbin/mysqld: Shutdown complete (mysqld 8.0.26)  MySQL Community Server - GPL.
[Entrypoint] Server shut down
[Entrypoint] Setting root user as expired. Password will need to be changed before database can be used.

[Entrypoint] MySQL init process done. Ready for start up.

[Entrypoint] Starting MySQL 8.0.26-1.2.4-server
2021-09-13T05:58:36.021824Z 0 [System] [MY-010116] [Server] /usr/sbin/mysqld (mysqld 8.0.26) starting as process 1
2021-09-13T05:58:36.032315Z 1 [System] [MY-013576] [InnoDB] InnoDB initialization has started.
2021-09-13T05:58:36.174361Z 1 [System] [MY-013577] [InnoDB] InnoDB initialization has ended.
2021-09-13T05:58:36.309322Z 0 [Warning] [MY-013746] [Server] A deprecated TLS version TLSv1 is enabled for channel mysql_main
2021-09-13T05:58:36.309489Z 0 [Warning] [MY-013746] [Server] A deprecated TLS version TLSv1.1 is enabled for channel mysql_main
2021-09-13T05:58:36.310439Z 0 [Warning] [MY-010068] [Server] CA certificate ca.pem is self signed.
2021-09-13T05:58:36.310659Z 0 [System] [MY-013602] [Server] Channel mysql_main configured to support TLS. Encrypted connections are now supported for this channel.
2021-09-13T05:58:36.336252Z 0 [System] [MY-011323] [Server] X Plugin ready for connections. Bind-address: '::' port: 33060, socket: /var/run/mysqld/mysqlx.sock
2021-09-13T05:58:36.336339Z 0 [System] [MY-010931] [Server] /usr/sbin/mysqld: ready for connections. Version: '8.0.26'  socket: '/var/lib/mysql/mysql.sock'  port: 3306  MySQL Community Server - GPL.
LM-SJC-11009966:~ pmalyalavenkatad$ mysql --version
-sh: mysql: command not found
LM-SJC-11009966:~ pmalyalavenkatad$ docker exec -it mysql bash
bash-4.4# mysql --version
mysql  Ver 8.0.26 for Linux on x86_64 (MySQL Community Server - GPL)
bash-4.4# myswl -uroot -p
bash: myswl: command not found
bash-4.4# mysql -uroot -p
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 16
Server version: 8.0.26

Copyright (c) 2000, 2021, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases
    -> ;
ERROR 1820 (HY000): You must reset your password using ALTER USER statement before executing this statement.
mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY 'new password'
    -> exit
    -> exit()
    -> ^C
mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY '5Uperm@n'
    -> ;
Query OK, 0 rows affected (0.01 sec)

mysql> 


