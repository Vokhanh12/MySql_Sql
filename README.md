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

<h4>Change types of column</h4>


```sql
ALTER TABLE [Table name]
MODIFY COLUMN [Column name] Type(size)

Example:
ALTER TABLE employees
MODIFY COLUMN email VARCHAR(100)
```

<h4>change position in column and Change types of column</h4>


```sql
ALTER TABLE [Table name]
MODIFY COLUMN [Column name] Type(size)
ALTER [Column name]

Example:
ALTER TABLE employees
MODIFY COLUMN email VARCHAR(20)
AFTER last_name
```


```bash
employee_id frist_name                                         last_name                                          email        ourly_pay hire_date        
----------- -------------------------------------------------- -------------------------------------------------- ------------ --------- ----------------
```

```sql
Example:
ALTER TABLE employees
MODIFY COLUMN email VARCHAR(20)
FRIST;
```


```bash
email         employee_id frist_name                                         last_name                                          ourly_pay hire_date        
------------  ----------- -------------------------------------------------- -------------------------------------------------- --------- ----------------
```

<h4>Insert Rows</h4>


```bash
employee_id frist_name                                         last_name                                          ourly_pay hire_date        phone_number
----------- -------------------------------------------------- -------------------------------------------------- --------- ---------------- ------------
```


```sql
INSERT INTO employees
VALUES (1, "Eugene", "Krabs", 25.50, "2023-01-02");
```


```bash
employee_id frist_name                                         last_name                                          ourly_pay hire_date        phone_number
----------- -------------------------------------------------- -------------------------------------------------- --------- ---------------- ------------
          1 Eugene                                             Krabs                                                  25.50       2023-01-02 0987654321  
```


```sql
INSERT INTO employees (employee_id, first_name, last_name, hourly_pay, hire_date, phone_number)
VALUES 
(2, 'SpongeBob', 'SquarePants', 20.00, '2023-03-15', '1234567890'),
(3, 'Patrick', 'Star', 18.50, '2023-03-20', '9876543210'),
(4, 'Squidward', 'Tentacles', 22.00, '2023-04-01', '5551112233'),
(5, 'Gary', 'Snail', 15.75, '2023-04-10', '8889990000'),
(6, 'Sandy', 'Cheeks', 30.00, '2023-05-01', '1112223333');
```


```bash
employee_id frist_name                                         last_name                                          ourly_pay hire_date        phone_number
----------- -------------------------------------------------- -------------------------------------------------- --------- ---------------- ------------
          1 Eugene                                             Krabs                                                  25.50       2023-01-02 0987654321  
          2 SpongeBob                                          SquarePants                                            20.00       2023-03-15 1234567890  
          3 Patrick                                            Star                                                   18.50       2023-03-20 9876543210  
          4 Squidward                                          Tentacles                                              22.00       2023-04-01 5551112233  
          5 Gary                                               Snail                                                  15.75       2023-04-10 8889990000  
          6 Sandy                                              Cheeks                                                 30.00       2023-05-01 1112223333 
```

