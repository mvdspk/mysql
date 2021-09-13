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
[click here](./dockerized-mysql.md).
