# My SQL 

## Login

```mysql
mysql -uroot -p
```

it asks for password, provide password and enter

## Exit mysql
 Type backward slash and alphabet q
```mysql
\q
```

## USer
### Change root user password

ALTER USER 'root'@'localhost' IDENTIFIED BY 'new password';

### Create new user
```mysql
CREATE USER 'username'@'localhost' IDENTOFOED BY 'password for the username'
```

### Grant user admin previleges

```mysql
GRANT ALL  PRIVILEGES ON * . * TO 'auser"@'localhost';
```

```mysql
FLUSH PRIVILEGES;
```

check for previliges on a user

```mysql
SHOW GRANTS FOR 'auser'@'localjost';
```

----

# Dockerized Container

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
