# MYSQL Syntax

## Create Database, Table

```mysql
CREATE DATABASE <database_name>
```

Create Table
```mysql
CREATE TABLE Test
(
    ID INT,
    Name VARCHAR(30),
    ReserveDate DATE,
    RoomNum INT
);
```

## INSERT 

```mysql
INSERT INTO TESTDB.inferjob VALUES (3, 2, 2, 'first', 'second', 2);
```

```mysql
INSERT INTO TESTDB.inferjob (platform, filetype, uploadPath, downloadPath, processStatus) VALUES (2, 1, 'file.mp4', 'file_out.mp4', 3)
```
