
## **Step 1: Table Creation & Insert Data**

**Table:** `Employees`

| Column Name | Data Type   | Constraints                 |
| ----------- | ----------- | --------------------------- |
| emp_id      | INT         | PRIMARY KEY                 |
| emp_name    | VARCHAR(50) | NOT NULL                    |
| salary      | INT         | CHECK (salary >= 0)         |
| gender      | CHAR(1)     | CHECK (gender IN ('M','F')) |
| department  | VARCHAR(50) | NOT NULL                    |
| company     | VARCHAR(50) | NOT NULL                    |

**SQL Query:**

```sql
CREATE TABLE Employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50) NOT NULL,
    salary INT CHECK (salary >= 0),
    gender CHAR(1) CHECK (gender IN ('M','F')),
    department VARCHAR(50) NOT NULL,
    company VARCHAR(50) NOT NULL
);

INSERT INTO Employees VALUES
(1, 'Rohit Sharma', 80000, 'M', 'IT', 'Google'),
(2, 'Sanya Malhotra', 75000, 'F', 'HR', 'Microsoft'),
(3, 'Anil Kumar', 60000, 'M', 'Finance', 'Zoho'),
(4, 'Priya Singh', 95000, 'F', 'IT', 'Apple'),
(5, 'Vikram Das', 70000, 'M', 'Sales', 'Tata'),
(6, 'Rina Patel', 85000, 'F', 'IT', 'Google'),
(7, 'Karan Verma', 72000, 'M', 'Finance', 'Microsoft'),
(8, 'Meera Joshi', 68000, 'F', 'HR', 'Zoho'),
(9, 'Arjun Rao', 78000, 'M', 'IT', 'Apple'),
(10, 'Sneha Kapoor', 64000, 'F', 'Sales', 'Tata'),
(11, 'Rahul Jain', 88000, 'M', 'Finance', 'Google'),
(12, 'Ananya Roy', 77000, 'F', 'HR', 'Microsoft'),
(13, 'Manish Sharma', 69000, 'M', 'IT', 'Zoho'),
(14, 'Pooja Mehta', 81000, 'F', 'Sales', 'Apple'),
(15, 'Vikas Gupta', 72000, 'M', 'IT', 'Tata'),
(16, 'Radhika Sen', 73000, 'F', 'Finance', 'Google'),
(17, 'Suresh Reddy', 76000, 'M', 'HR', 'Microsoft'),
(18, 'Divya Nair', 80000, 'F', 'IT', 'Zoho'),
(19, 'Amitabh Das', 85000, 'M', 'Sales', 'Apple'),
(20, 'Neha Sharma', 70000, 'F', 'IT', 'Tata'),
(21, 'Siddharth Verma', 95000, 'M', 'Finance', 'Google'),
(22, 'Isha Khanna', 68000, 'F', 'HR', 'Microsoft'),
(23, 'Deepak Joshi', 72000, 'M', 'IT', 'Zoho'),
(24, 'Anjali Kapoor', 80000, 'F', 'Sales', 'Apple'),
(25, 'Ramesh Kumar', 75000, 'M', 'IT', 'Tata'),
(26, 'Tanya Singh', 90000, 'F', 'Finance', 'Google'),
(27, 'Vijay Rao', 77000, 'M', 'HR', 'Microsoft'),
(28, 'Rekha Sharma', 68000, 'F', 'IT', 'Zoho'),
(29, 'Kunal Mehta', 85000, 'M', 'Sales', 'Apple'),
(30, 'Simran Patel', 72000, 'F', 'IT', 'Tata');
```

---

## Step 2: Questions

### Easy

1. Display all employee details.
2. Display `emp_name`, `salary`, and `company` of all employees.
3. Show employees working in the `IT` department.
4. Show employees with salary greater than 80,000.

### Moderate

5. Display employees ordered by `salary` descending.
6. Count the number of employees in each `company`.
7. Find the average salary in each `department`.
8. Display female employees in the `Finance` department.
9. Increase salary of all employees in `Tata` by 5,000.
10. Delete employees with salary less than 65,000.

### Tough (2 Queries)

11. Display the top 3 highest-paid employees in the `IT` department.
12. Find companies where the **average salary of male employees is greater than 75,000**.

---
