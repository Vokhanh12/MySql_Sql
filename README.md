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
  [Row name] [Types](size),  
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

