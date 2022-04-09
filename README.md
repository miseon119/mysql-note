# mysql-note

## Install mysql in ubuntu 18.04

```bash
sudo apt-get update
sudo apt-get install mysql-server
sudo ufw allow mysql
sudo systemctl start mysql
sudo systemctl enable mysql
sudo /usr/bin/mysql -u root -p
```

Check user info
```bash
mysql> SELECT User, Host, authentication_string FROM mysql.user;
```

## Hello world mysql

```bash
mysql> CREATE DATABASE TESTDB;
mysql> SHOW DATABASES;
```

Generate user ID:
```bash
mysql> CREATE USER 'testuser'@'localhost' IDENTIFIED BY 'your_password';
mysql> FLUSH PRIVILEGES;
mysql> SELECT User, Host, authentication_string FROM mysql.user;
```

Give user a priority to access TESTDB
```bash
mysql> GRANT ALL PRIVILEGES ON TESTDB.* TO 'testuser'@'localhost';
mysql> FLUSH PRIVILEGES;
mysql> SHOW GRANTS FOR'testuser'@'localhost';
mysql> SELECT User, Host, authentication_string FROM mysql.user;
```

## Version Check
```bash
mysql> show variables like "%version%";
```

## Change Password
```bash
mysql> SET PASSWORD FOR 'root'@'localhost' = PASSWORD('newpassword');
```

