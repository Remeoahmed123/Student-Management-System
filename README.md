#  Student Management System (SQL Project)

---

##  Project Description

The **Student Management System** is a relational database project developed using **MySQL**. It is designed to manage student records, departments, courses, and fee details efficiently.

This system demonstrates how academic data can be stored, linked, and analyzed using SQL queries.

---

##  Overview

This project is based on a **relational database model**, where multiple tables are connected using keys. It manages student information along with their department, enrolled courses, and fee status.

The system uses SQL queries to retrieve meaningful information by combining data from multiple tables.

---

##  Objectives

* To design a student database system
* To manage student, department, course, and fee data
* To understand relationships between tables
* To practice SQL queries (SELECT, JOIN)
* To analyze student fee records

---

##  Technologies Used

* MySQL
* SQL (Structured Query Language)

---

##  Database Structure

###  Students Table

| Column Name | Description       |
| ----------- | ----------------- |
| student_id  | Unique student ID |
| name        | Student name      |
| age         | Student age       |
| city        | Student city      |
| dept_id     | Linked department |

---

###  Departments Table

| Column Name | Description          |
| ----------- | -------------------- |
| dept_id     | Unique department ID |
| dept_name   | Department name      |
| location    | Department location  |

---

###  Courses Table

| Column Name | Description       |
| ----------- | ----------------- |
| course_id   | Unique course ID  |
| course_name | Course name       |
| dept_id     | Linked department |

---

###  Fees Table

| Column Name | Description    |
| ----------- | -------------- |
| fee_id      | Unique fee ID  |
| student_id  | Linked student |
| amount      | Fee amount     |
| status      | Paid / Pending |

---

##  Relationships

* Each student belongs to one department
* Each department can have multiple students
* Each course is linked to a department
* Each fee record is linked to a student

---

##  Key Features

* Store student details
* Manage departments and courses
* Track student fees
* Perform JOIN queries
* Analyze fee status

---

##  Sample SQL Queries

###  Students + Fees

```sql
SELECT s.name, f.amount, f.status
FROM students s
JOIN fees f ON s.student_id = f.student_id;
```

###  Students + Departments

```sql
SELECT s.name, d.dept_name
FROM students s
JOIN departments d ON s.dept_id = d.dept_id;
```

---

##  Output Explanation

The system generates combined data using SQL JOIN operations.

### Output Includes:

* Student names with their fee amount and status
* Student names with their department

### Explanation:

* The JOIN operation connects tables using keys like `student_id` and `dept_id`
* It helps display related data from multiple tables in a single result

### Example Output:

| Name   | Amount | Status  |
| ------ | ------ | ------- |
| ALI    | 50000  | Paid    |
| AYESHA | 70000  | Pending |
| AHMED  | 80000  | Paid    |
| ALINA  | 90000  | Paid    |

This output shows:

* Fee payment status of each student
* Which students have paid or pending fees
<img width="807" height="173" alt="Output" src="https://github.com/user-attachments/assets/250a6156-95bd-421f-ae2f-4d18be40eec3" />

##  Conclusion

This project demonstrates how relational databases work by linking multiple tables. It shows how SQL JOIN queries can be used to retrieve meaningful academic and financial information.

---
