


## Question 1: Table Creation & Insert Data 

**Task:** Create a table `Employees` with the following structure and insert 5–6 records.

**Table Structure:**

| Column Name | Data Type   | Constraints                |
| ----------- | ----------- | -------------------------- |
| emp_id      | INT         | PRIMARY KEY                |
| emp_name    | VARCHAR(50) | NOT NULL                   |
| salary      | INT         | CHECK(salary > 0)          |
| gender      | CHAR(1)     | CHECK(gender IN ('M','F')) |
| dept        | VARCHAR(50) | NOT NULL                   |
| company     | VARCHAR(50) |                            |

**Sample Query:**

```sql
CREATE TABLE Employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50) NOT NULL,
    salary INT CHECK(salary > 0),
    gender CHAR(1) CHECK(gender IN ('M','F')),
    dept VARCHAR(50) NOT NULL,
    company VARCHAR(50)
);

INSERT INTO Employees VALUES
(1, 'Ravi Kumar', 50000, 'M', 'CSE', 'TechCorp'),
(2, 'Sita Reddy', 60000, 'F', 'ECE', 'InnovateX'),
(3, 'Rahul Sharma', 45000, 'M', 'ME', 'BuildIt'),
(4, 'Anjali Patel', 55000, 'F', 'CSE', 'TechCorp'),
(5, 'Vikram Singh', 70000, 'M', 'EEE', 'InnovateX'),
(6, 'Meena Joshi', 65000, 'F', 'ME', 'BuildIt');
```

---

## **Easy Queries**

1. Display all employees.
2. Display `emp_name` and `salary` only.
3. Display all employees in the `CSE` department.
4. Display all female employees.

---

## **Moderate Queries**

1. Display employees with salary greater than 55000.
2. Display employees in ascending order of salary.
3. Display employees in `TechCorp` whose salary is less than 60000.
4. Update salary of `emp_id = 3` to 48000.
5. Delete employee with `emp_id = 5`.

---

## **Aggregate & Grouping Queries (Moderate)**

1. Find the average salary of all employees.
2. Find the maximum and minimum salary.
3. Count employees in each department.
4. Display the total salary paid by each company.

---

## **Tough Query**

**Scenario:** Find employees whose salary is **above the average salary of their department**, and display their `emp_name`, `salary`, `dept`, and `company`.

**Query Example:**

```sql
SELECT emp_name, salary, dept, company
FROM Employees e
WHERE salary > (
    SELECT AVG(salary)
    FROM Employees
    WHERE dept = e.dept
);
```

---


