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
