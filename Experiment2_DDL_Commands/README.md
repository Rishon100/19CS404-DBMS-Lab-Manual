# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
<img width="1235" height="405" alt="image" src="https://github.com/user-attachments/assets/1bfe84c8-54ac-4804-bd3c-c7e495a158ca" />


```
INSERT INTO Employee (EmployeeID, Name, Department, Salary)
SELECT EmployeeID, Name, Department, Salary FROM Former_employees;
```

**Output:**

<img width="1226" height="390" alt="image" src="https://github.com/user-attachments/assets/e428dcdf-bd60-4c84-bf90-0bd0a2030d8d" />


**Question 2**
---
<img width="1259" height="472" alt="image" src="https://github.com/user-attachments/assets/ce9f0d0b-79f0-44a1-853d-918e4cf490b1" />


```
create table contacts(
contact_id integer primary key,
first_name text not null,
last_name text not null,
email text,
phone text not null check (length(phone)>=10)
);
```

**Output:**
<img width="1247" height="419" alt="image" src="https://github.com/user-attachments/assets/5f6438a9-1575-4aa3-9b09-cbe92d95f5c9" />


**Question 3**
---
<img width="1228" height="409" alt="image" src="https://github.com/user-attachments/assets/c0acbea7-4357-4958-8448-4712165366ee" />


```
create table Department(
DepartmentID integer primary key,
DepartmentName text unique not null,
Location text);
```

**Output:**

<img width="1243" height="406" alt="image" src="https://github.com/user-attachments/assets/e003e5a5-e4c8-47fb-83d5-27cba288fb7a" />


**Question 4**
---
<img width="1241" height="318" alt="image" src="https://github.com/user-attachments/assets/3623bf9c-cd6f-4525-ace4-0185ba069a7d" />


```
insert into Student_details(RollNo,Name,Gender,Subject,Marks)
values(201,'David Lee','M','Physics',92);
```

**Output:**

<img width="1250" height="333" alt="image" src="https://github.com/user-attachments/assets/af74282d-3281-467a-9421-2afff6c35961" />


**Question 5**
---
<img width="1238" height="444" alt="image" src="https://github.com/user-attachments/assets/7f631be1-6440-49d4-9477-806b530d6629" />


```
alter table student_details add column ParentsNumber number;
alter table student_details add column Adhar_Number number;
```

**Output:**

<img width="1241" height="439" alt="image" src="https://github.com/user-attachments/assets/12e87c14-3406-4243-ac3f-edeebf3b38d1" />


**Question 6**
---
<img width="1249" height="440" alt="image" src="https://github.com/user-attachments/assets/1922141d-8c19-4610-ba73-1c5f477ed08d" />


```
create table Locations(
LocationID INTEGER,
LocationName TEXT,
Address TEXT);
```

**Output:**

<img width="1259" height="495" alt="image" src="https://github.com/user-attachments/assets/92d0b3ae-a55b-4a97-941d-b1355fec33ae" />


**Question 7**
---
<img width="1228" height="506" alt="image" src="https://github.com/user-attachments/assets/e69b63ab-817d-400d-9b77-6d5bdaf6e641" />

```
create table Products(
ProductID INTEGER,
ProductName TEXT,
Price REAL,
Stock INTEGER);
```

**Output:**
<img width="1263" height="425" alt="image" src="https://github.com/user-attachments/assets/638c59ad-6191-4b3e-8063-cae21bec0ffb" />


**Question 8**
---
<img width="1235" height="309" alt="image" src="https://github.com/user-attachments/assets/dbe3d49b-dbae-4f13-82ca-0105f18c1af6" />


```
insert into Employee(EmployeeID,Name,Position,Department,Salary)
values (001,'Sarah Parker','Manager','HR',60000);
```

**Output:**

<img width="1254" height="349" alt="image" src="https://github.com/user-attachments/assets/097c040d-49ff-489b-a5c6-1217396f73dd" />


**Question 9**
---<img width="1229" height="528" alt="image" src="https://github.com/user-attachments/assets/70ca5d22-b43b-4f65-aec1-3f7d5e1c6d36" />


```
alter table books add column ISBN varchar(30);
alter table books add column domain_dept varchar(30);
```

**Output:**

<img width="1253" height="494" alt="image" src="https://github.com/user-attachments/assets/2b68ff03-9f8d-47b4-8495-ae16794c6d9e" />


**Question 10**
---
<img width="1247" height="525" alt="image" src="https://github.com/user-attachments/assets/a5321d1d-d9df-41e9-911b-08138f624f57" />

```
create table Reviews(
ReviewID INTEGER,
ProductID INTEGER,
Rating REAL,
ReviewText TEXT);```

**Output:**

<img width="1252" height="501" alt="image" src="https://github.com/user-attachments/assets/49b18c69-08b1-403b-a919-42c823c760e5" />



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
