Microsoft Windows [Version 10.0.22621.1848]
(c) Microsoft Corporation. All rights reserved.

C:\Users\HP>cd..

C:\Users>cd..

C:\>cd xampp

C:\xampp>cd mysql

C:\xampp\mysql>cd bin

C:\xampp\mysql\bin>mysql.exe -u root
ERROR 2002 (HY000): Can't connect to MySQL server on 'localhost' (10061)

C:\xampp\mysql\bin>mysql.exe -u root
ERROR 2002 (HY000): Can't connect to MySQL server on 'localhost' (10061)

C:\xampp\mysql\bin>mysql -u root -p
Enter password:
ERROR 2002 (HY000): Can't connect to MySQL server on 'localhost' (10061)

C:\xampp\mysql\bin>mysql -u root -p
Enter password:
ERROR 2002 (HY000): Can't connect to MySQL server on 'localhost' (10061)

C:\xampp\mysql\bin>mysql -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.25-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show tables
    -> ;
ERROR 1046 (3D000): No database selected
MariaDB [(none)]> show tables:
    -> ;
ERROR 1046 (3D000): No database selected
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| bottle             |
| chandu             |
| information_schema |
| juli               |
| lucky              |
| mysql              |
| performance_schema |
| phpmyadmin         |
| sanjay             |
| sanju              |
| shiva              |
| test               |
+--------------------+
12 rows in set (0.038 sec)

MariaDB [(none)]> create database siva;
Query OK, 1 row affected (0.001 sec)

MariaDB [(none)]> create table details(name varchar(10),phone int,roll int);
ERROR 1046 (3D000): No database selected
MariaDB [(none)]> use database siva;
ERROR 1049 (42000): Unknown database 'database'
MariaDB [(none)]> use siva;
Database changed
MariaDB [siva]> create table details(name varchar(10),phone int,roll int);
Query OK, 0 rows affected (0.037 sec)

MariaDB [siva]> desc details;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| name  | varchar(10) | YES  |     | NULL    |       |
| phone | int(11)     | YES  |     | NULL    |       |
| roll  | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.024 sec)

MariaDB [siva]> insert into details values("siva",8890057373,34567866378);
Query OK, 1 row affected, 2 warnings (0.058 sec)

MariaDB [siva]> show table;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near '' at line 1
MariaDB [siva]> select * from details;
+------+------------+------------+
| name | phone      | roll       |
+------+------------+------------+
| siva | 2147483647 | 2147483647 |
+------+------------+------------+
1 row in set (0.001 sec)

MariaDB [siva]> update details values("sanjay");
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'values("sanjay")' at line 1
MariaDB [siva]> insert into details values("sanjay",6890099875,674748490);
Query OK, 1 row affected, 1 warning (0.008 sec)

MariaDB [siva]> select * from details;
+--------+------------+------------+
| name   | phone      | roll       |
+--------+------------+------------+
| siva   | 2147483647 | 2147483647 |
| sanjay | 2147483647 |  674748490 |
+--------+------------+------------+
2 rows in set (0.000 sec)

MariaDB [siva]>
