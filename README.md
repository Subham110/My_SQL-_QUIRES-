# My SQL QUIRES

This structure explains how to create and manipulate a SQL database and tables, and includes examples of various SQL operations.


# SQL Database and Table Operations
This repository contains SQL commands and queries that demonstrate how to create and manipulate databases and tables in SQL.

# 1. Show Existing Databases
To list all databases on the server:
```sql
SHOW DATABASES;
```

# 2. Create a New Database
To create a new database:
```sql
CREATE DATABASE my_Data;
```

# 3. Use the Database
To select and use the newly created database:
```sql
USE my_Data;
```

# 4. Show Existing Tables
To list all tables in the selected database:
```sql
SHOW TABLES;
```

# 5. Create a New Table
To create a table named `class_1`:
```sql
CREATE TABLE class_1 (
    ID TEXT(10),
    Name VARCHAR(20),
    Phone_NO INT(10),
    DOB DATE);
```

# 6. Describe the Table Structure
To view the structure of the `class_1` table:
```sql
DESC class_1;
```

# 7. Insert Data into the Table
To insert records into the `class_1` table:
```sql
INSERT INTO class_1 (Id, Name, Phone_No, DOB) 
VALUES (1, "Subham", 7854926631, '2003-03-23');

INSERT INTO class_1 
VALUES (2, "Ritu", 7639862543, '2004-07-12');

INSERT INTO class_1 (Id, Name, Phone_No) 
VALUES (3, "Lucifer", 7854763891);
```

# 8. Select Data from the Table
To retrieve all records from the `class_1` table:
```sql
SELECT * FROM class_1;
```

To retrieve specific columns:
```sql
SELECT ID FROM class_1;
SELECT Name FROM class_1;
SELECT Phone_No FROM class_1;
SELECT DOB FROM class_1;
```

# 9. Update, Alter, Delete, and Drop Operations
- Update a record:
    ```sql
    UPDATE class_1 SET DOB = '2005-09-29' WHERE ID = 3;
    ```
- Alter the table structure:
    ```sql
    ALTER TABLE class_1 ADD Email TEXT(20);
    ```
- Delete a record:
    ```sql
    DELETE FROM class_1 WHERE Id = 5;
    ```
- Drop a column:
    ```sql
    ALTER TABLE class_1 DROP Email;
    ```

# 10. Primary Key Example
To create a new table with a primary key:
```sql
CREATE TABLE class_2 (
    Roll_No INT(10) NOT NULL PRIMARY KEY,
    Student_Name VARCHAR(20),
    Address VARCHAR(40),
    Phone_No INT(10));
```

# 11. Join Operations
To perform an inner join between two tables:
```sql
SELECT student.Roll_No, student.Name, student.Class, student_data.DOB, student_data.Phone_No 
FROM student 
INNER JOIN student_data ON student.Roll_No = student_data.Roll_No;
```

To perform a left join:
```sql
SELECT * FROM student 
LEFT JOIN student_data ON student.Roll_No = student_data.Roll_No;
```

# Conclusion
This repository provides basic examples of SQL operations including creating databases and tables, inserting and querying data, and performing join operations. These examples are essential for anyone starting with SQL and looking to understand fundamental database management.

