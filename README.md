# EX-3-SubQueries, Views and Joins 


## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![1](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/0dcf22b5-d8d4-478e-9764-4a5a2dd72ef6)

### OUTPUT:
![2](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/889c2211-3762-43ff-9910-fb12b5e80466)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![3](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/c531ca39-0e8d-4b73-beef-647329f48611)



### OUTPUT:
![4](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/f71b2b17-f521-4864-8deb-810df5c7e9ce)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![5](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/8f13bceb-db30-4841-8291-d8db28f8992e)


### OUTPUT:
![6](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/a67e36e9-72af-4e77-9fb1-c6cb2064cd8d)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![7](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/5bc2600e-b977-4399-b78c-b3145adc0990)



### OUTPUT:
![8](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/59270e8d-9ce7-4fde-aad5-03cc65b2af20)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
![9](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/d6f6b325-9657-4c62-9b6b-326e2a797f02)



### OUTPUT:
![10](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/6279ab83-81c1-4c44-8045-c745eb3cdc7f)


### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![11](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/1d06e37d-d937-4b4a-a750-6f8334581215)



### OUTPUT:
![12](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/27105a3e-0587-473d-ab27-0eb11a69fc96)


## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![13](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/f0875d23-2619-48e6-8915-b201d8161c54)



### OUTPUT:
![14](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/4eccd970-a60f-469e-8b20-54728446ad73)


### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![15](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/5c1d6777-7080-4be9-b32e-ddd14fbc3790)


### OUTPUT:
![16](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/38f36503-1fe6-4325-8299-981de735fe51)

### Q9) Perform Natural join on both tables

### QUERY:
![17](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/8eee4d01-feae-41b7-bb48-72516d0d8345)

### OUTPUT:
![18](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/b54b0b3e-4f37-4dc2-b5d8-65430a937035)

### Q10) Perform Left and right join on both tables

### QUERY:
   ## Left Join
![19](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/2adb4484-2d48-4179-b76a-3e8df01ba8e6)

## right join
![19](https://github.com/SASIRAJ27/EX-3-SubQueries-Views-and-Joins/assets/113497176/0eba2687-babc-4b45-b498-0942d6cfaba5)



### OUTPUT:
   ## Left Join
   ![image](https://github.com/DhanushPalani/EX-3-SubQueries-Views-and-Joins/assets/121594640/f7e2b17f-33d1-404c-8a43-83636dc8c552)


   ## Right Join
   ![image](https://github.com/DhanushPalani/EX-3-SubQueries-Views-and-Joins/assets/121594640/43cc7093-35af-4c4b-8854-068a0f0b34d1)
