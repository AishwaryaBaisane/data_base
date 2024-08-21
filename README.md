# data_base

## CREATE TABLE
## Field names: id, name, role, salary, age, address, phone.
```dart
CREATE TABLE "employee" (

	"id"	INTEGER,
	"name"	TEXT NOT NULL,
	"role"	TEXT NOT NULL,
	"salary"	INTEGER,
	"age"	INTEGER NOT NULL,
	"address"	TEXT,
	"phone"	INTEGER NOT NULL,
	PRIMARY KEY("id" AUTOINCREMENT)

);
 
``` 

## Add a new employee with all the details
```dart
INSERT INTO employee(name,role,salary,age,address,phone) VALUES('Aishawarya','Flutter Developer',100000,20,'201,dhruv Park Soc,surat',2538172972);
```
## Insert emloyees data
- Add multiple employees with selective data:
```dart
INSERT INTO employee(name,role,salary,age,address,phone) VALUES ('Aishawarya','Flutter Developer',100000,20,'201,dhruv Park Soc,surat',2538172972);
INSERT INTO employee(name,role,salary,age,address,phone) VALUES ('Prachi','Flutter Developer',50000,21,'6501,shanti nagar , surat' , 361728134);
INSERT INTO employee(name,role,salary,age,address,phone) VALUES ('Rahul','FullStack Develoer',60000,25,'167,Shree ji society,surat',1357278342);
INSERT INTO employee(name,role,salary,age,address,phone) VALUES ('Devanshu','Ui-Ux Designer',80000,25,'100,Parvat Gam,surat',1362738274);
INSERT INTO employee(name,role,salary,age,address,phone) VALUES ('Charmi','Ui-Ux Designer',90000,23,'502,ShivDarshan society,surat',136772883);
 
``` 

## Read data
- Retrieve all employee information:
```dart
  SELECT * FROM   employee;
```
## Get specific columns for all employees (e.g., name, salary)
```dart
SELECT  name,salary FROM employee WHERE name =name;
```
## Find employees with a particular role (e.g., Manager):
```dart
SELECT  name,role FROM employee WHERE role ='Flutter Devloper';
```

## Search for employees with names containing "An" (case-insensitive):

```dart
SELECT  name FROM employee WHERE name LIKE 'S%';
```
## Find employees older than 20 and earning more than 25,000:

```dart
SELECT * FROM employee WHERE  (salary>25000)AND age>20;
```
## Change the salary of an employee with ID 1:

```dart
UPDATE employee
SET salary = 50000
WHERE id =1
```
## Update the address for employees in the 'Flutter Devloper' role:

```dart
UPDATE employee SET address = '201,dhruv Park Soc,surat' WHERE role  = 'Flutter Devloper';
```

## Remove an employee with ID 101:
```dart
DELETE FROM employee WHERE id = 3;
```

## Delete all employees under 20 (assuming it's not a valid age).

```dart
DELETE FROM employee WHERE age <24;
```
<img src  = "https://github.com/user-attachments/assets/9ac0b7a2-ca2e-4186-873f-d77b08ed15b0" height=40%  width=30%>


