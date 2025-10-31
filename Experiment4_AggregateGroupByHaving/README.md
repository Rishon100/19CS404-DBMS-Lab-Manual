# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
<img width="1223" height="412" alt="Screenshot 2025-10-17 231458" src="https://github.com/user-attachments/assets/ffdc3816-8b35-4cd5-8fdf-28b64668afc1" />


```sql
INSERT INTO Employee (EmployeeID, Name, Department, Salary)
SELECT EmployeeID, Name, Department, Salary FROM Former_employees;
```

**Output:**

<img width="1245" height="376" alt="Screenshot 2025-10-17 231508" src="https://github.com/user-attachments/assets/634e41b5-7bab-47ba-a448-f1ff796ede06" />

**Question 2**
---
<img width="1242" height="457" alt="Screenshot 2025-10-17 231516" src="https://github.com/user-attachments/assets/f9b7801c-28c3-4f70-b7b5-f65c1f10c4a9" />

```sql
create table contacts(
contact_id integer primary key,
first_name text not null,
last_name text not null,
email text,
phone text not null check (length(phone)>=10)
);
```

**Output:**

<img width="1235" height="419" alt="Screenshot 2025-10-17 231522" src="https://github.com/user-attachments/assets/f267f973-40f5-4cd5-855d-73f811164193" />


**Question 3**
---
<img width="1253" height="420" alt="Screenshot 2025-10-17 231530" src="https://github.com/user-attachments/assets/003add0b-87c2-44e9-b38d-321af8c04170" />

```sql
create table Department(
DepartmentID integer primary key,
DepartmentName text unique not null,
Location text);
```

**Output:**

<img width="1229" height="380" alt="Screenshot 2025-10-17 231535" src="https://github.com/user-attachments/assets/5418e4d5-7aaa-4d7f-ace5-b94856f13c40" />

**Question 4**
---
<img width="1229" height="314" alt="image" src="https://github.com/user-attachments/assets/a7bc0041-e20b-4917-aa6e-b4bd28206ff4" />


```sql
insert into Student_details(RollNo,Name,Gender,Subject,Marks)
values(201,'David Lee','M','Physics',92);
```

**Output:**

<img width="1250" height="325" alt="image" src="https://github.com/user-attachments/assets/6dc72ca9-5ea4-475b-a2fb-2a3677c08d01" />

**Question 5**
---
<img width="1249" height="447" alt="image" src="https://github.com/user-attachments/assets/e3488677-9325-41f9-bacc-d2d98d9b7d1f" />


```sql
alter table student_details add column ParentsNumber number;
alter table student_details add column Adhar_Number number;
```


**Output:**

<img width="1241" height="491" alt="image" src="https://github.com/user-attachments/assets/1af841d9-4f95-4114-9264-dbfb61615645" />

**Question 6**
---
<img width="1252" height="461" alt="image" src="https://github.com/user-attachments/assets/73c1ae28-68c9-404a-bded-9ef715143504" />


```sql
create table Locations(
LocationID INTEGER,
LocationName TEXT,
Address TEXT);
```

**Output:**

<img width="1231" height="493" alt="image" src="https://github.com/user-attachments/assets/b438bcd1-10dc-443b-b3df-7d79d8c96505" />

**Question 7**
---
<img width="1244" height="517" alt="image" src="https://github.com/user-attachments/assets/36b091de-be16-4799-b15e-da578c99f077" />


```sql
create table Products(
ProductID INTEGER,
ProductName TEXT,
Price REAL,
Stock INTEGER);
```

**Output:**

<img width="1243" height="424" alt="image" src="https://github.com/user-attachments/assets/5a178317-541e-44bf-81ec-78e150f9263b" />

**Question 8**
---
<img width="1243" height="314" alt="image" src="https://github.com/user-attachments/assets/e3db1e2c-c7e0-4740-9530-c44258f1b69d" />


```sql
insert into Employee(EmployeeID,Name,Position,Department,Salary)
values (001,'Sarah Parker','Manager','HR',60000);
```
**Output:**

<img width="1262" height="357" alt="image" src="https://github.com/user-attachments/assets/0f6b7227-400f-4fbe-b9a1-5e8999db00ac" />

**Question 9**
---
<img width="1238" height="523" alt="image" src="https://github.com/user-attachments/assets/35e0f498-34ba-424f-bec1-8668ff5750a2" />


```sql
alter table books add column ISBN varchar(30);
alter table books add column domain_dept varchar(30);
```

**Output:**

<img width="1246" height="480" alt="image" src="https://github.com/user-attachments/assets/1fec11de-af54-4c59-b911-32de88d3b7a6" />

**Question 10**
---
<img width="1252" height="522" alt="image" src="https://github.com/user-attachments/assets/0a314811-d4c9-4608-bec7-d730b05d5bc2" />


```sql
create table Reviews(
ReviewID INTEGER,
ProductID INTEGER,
Rating REAL,
ReviewText TEXT);
```


**Output:**

<img width="1259" height="508" alt="image" src="https://github.com/user-attachments/assets/43c54d45-d9a1-4439-b040-a75c1abc27e6" />

## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
