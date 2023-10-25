# MySql_Sql
# MySQL SQL tutorial for beginners
# Link : https://www.youtube.com/watch?v=5OdVJbNCSso&t=843s


<h4>Create Database</h4>  


```sql  
CREATE DATABASE [DATABASE NAME]  
USE [DATABASE NAME]  
```


<h4>Create table</h4>  


```sql  
CREATE TABLE [Table Name] (  
  [Column name] [Types](size),  
  ...  
);

Type: Int, Varchar, Decimal, Date...

Example:

CREATE TABLE employees (  
  employee_id INT,  
  frist_name VARCHAR(50),  
  last_name VARCHAR(50),  
  hourly_pay DECIMAL(5,2),  
  hire_date DATE,  
  );  
```

```bash
employee_id frist_name                                         last_name                                          ourly_pay hire_date       
----------- -------------------------------------------------- -------------------------------------------------- --------- ----------------
```

<h4>Drop table</h4>

```sql
DROP TABLE [Table name]
```


<h4>add a new column</h4>


```sql
ALTER TABLE [Table name]
ADD [Column name]

Example:
ALTER TABLE employees
ADD phone_number VARCHAR(10);
```

```bash
employee_id frist_name                                         last_name                                          ourly_pay hire_date        phone_number
----------- -------------------------------------------------- -------------------------------------------------- --------- ---------------- ------------
```

<h4>rename column</h4>


```sql
ALTER TABLE [Table name]
RENAME COLUMN [Column after] to [Column before]

Example:
ALTER TABLE employees
RENAME COLUMN phone_number TO email;
```


```bash
employee_id frist_name                                         last_name                                          ourly_pay hire_date        email
----------- -------------------------------------------------- -------------------------------------------------- --------- ---------------- ------------

```






