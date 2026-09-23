mysql> USE sales;
Database changed
mysql> -- or
mysql> USE week3_db;
ERROR 1049 (42000): Unknown database 'week3_db'
mysql> CREATE TABLE student (
    ->     id INT PRIMARY KEY,
    ->     fullName VARCHAR(100),
    ->     age INT
    -> );
Query OK, 0 rows affected (1.33 sec)

mysql> INSERT INTO student (id, fullName, age) VALUES
    ->     (1, 'Alice Johnson', 19),
    ->     (2, 'Brian Kamau', 21),
    ->     (3, 'Catherine Odhiambo', 20);
Query OK, 3 rows affected (0.06 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> SELECT * FROM student;
+----+--------------------+------+
| id | fullName           | age  |
+----+--------------------+------+
|  1 | Alice Johnson      |   19 |
|  2 | Brian Kamau        |   21 |
|  3 | Catherine Odhiambo |   20 |
+----+--------------------+------+
3 rows in set (0.01 sec)

mysql> UPDATE student
    -> SET age = 20
    -> WHERE id = 2;
Query OK, 1 row affected (0.04 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> SELECT * FROM student WHERE id = 2;
+----+-------------+------+
| id | fullName    | age  |
+----+-------------+------+
|  2 | Brian Kamau |   20 |
+----+-------------+------+
1 row in set (0.00 sec)

mysql>
