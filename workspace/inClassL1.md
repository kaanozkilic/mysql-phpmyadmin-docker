## In-Class Task 1: Getting Started with Database

You are required to complete the following tasks in-class on the same day and push it to GitHub. (1 point)

1. Write a SQL statement to create a new database named fname_lname (replace fname and lname with your first and last name, respectively).

```
mysql> CREATE DATABASE kaan_ozkilic;
Query OK, 1 row affected (0.04 sec)
```

2. Use the SHOW DATABASES; command to verify that the database has been created.

```
mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| kaan_ozkilic       |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.01 sec)
```

3. Write a SQL statement to set the newly created database fname_lname as the current database.

```
mysql> USE kaan_ozkilic;
Database changed
```

4. Write a SQL statement to to create a new database named database24. 

```
CREATE DATABASE database24;
Query OK, 1 row affected (0.08 sec)
```

5. Write a SQL statement to drop the fname_lname database.

```
mysql> DROP DATABASE IF EXISTS kaan_ozkilic;
Query OK, 0 rows affected (0.08 sec)
```

6. Write a SQL statement to set the newly created database database24 as the current database.

```
mysql> USE database24;
Database changed
```

6. Write a SQL statement to display the list of tables in the selected database. 

```
mysql> SHOW TABLES;
Empty set (0.01 sec)
```

7. Run the following SQL statement to create a table in database24. 

```
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE
);
```

```
mysql> CREATE TABLE students (
    -> id INT AUTO_INCREMENT PRIMARY KEY,
    -> first_name VARCHAR(50) NOT NULL,
    -> last_name VARCHAR(50) NOT NULL,
    -> email VARCHAR(100) UNIQUE
    -> );
Query OK, 0 rows affected (0.33 sec)
```
