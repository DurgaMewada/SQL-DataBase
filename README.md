# SQL DataBase

## What is SQLite?
- SQL stands for Structured Query Language
- SQL lets you access and manipulate databases
- SQL became a standard of the American National Standards Institute (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987

### 1. Creating Table

```sql
CREATE TABLE "employee" (
    "id" INTEGER NOT NULL,
    "name" TEXT NOT NULL,
    "role" TEXT,
    "salary" INTEGER NOT NULL,
    "age" INTEGER NOT NULL,
    "address" TEXT,
    "phone" INTEGER NOT NULL,
    PRIMARY KEY("id" AUTOINCREMENT)
);
```
### 2. Inserting Data

- Add a new employee with all details:

  ``` sql
  INSERT INTO employees (id, name, role, salary, age, address, phone) VALUES (1, "Durga Mewada", "Manager", 50000, 20, "910 Surat", 9313381084);
  ```

- Add multiple data with selective values:

  ``` sql
     INSERT INTO employees (name, role, salary, age, address, phone) VALUES 
    ("Mayuri Prohit", " Application Developer", 60000, 25, "138 Mumbai", 9382756937),
    ("Snehal Gulale", "Web Developer", 65000, 30, "143 Delhi", 9675583753),
    ("Anita Mewada", "HOD", 66000, 29, "27 Surat ", 8795736626),
    ("Nirmala Rajvansi", "Designer", 72000, 45, "387 Pune", 9313381084),
    ("Abhishek Malahan ", "Manager", 61000, 27, "142 Hydarbad", 9104294560),
    ("Jasvant Patel", "Accountant", 54000, 31, "211 Ankleshwar", 9974789975);
  ```

### 3. Retrieve Data
  - Retrieve all employee information:

    ``` sql
    SELECT * FROM employees;

    ```
  - Get specific columns for all employees (e.g., name, salary):

    ``` sql
    SELECT name, salary FROM employees;


    ```

  - Find employees with a particular role (e.g., Manager):

    ``` sql
    SELECT * FROM employees WHERE role = "Manager";

    ```

  - Search for employees with names containing "An" (case-insensitive):
    ``` sql
    SELECT * FROM employees WHERE name LIKE "%An%";


    ```

  - Find employees older than 30 and earning more than $70,000:

    ``` sql
    SELECT * FROM employees WHERE age > 30 AND salary > 70000;

vDeveloper
    ```


### 4. Update Employee Records

- Change the salary of an employee with ID 5:
    ```sql
    UPDATE employees SET salary = 15000 WHERE name =  "Jasvant Patel";

    ```
- Update the address for employees in the 'Sales' role:
    ```sql
    UPDATE employees SET address = "143 Delhi" WHERE role = "Web Developer ";

    ```


### 5. Delete Employee Records
    
- Remove an employee with ID 10:
    ```sql
    DELETE FROM employees WHERE id = 10;

    ```



- Delete all employees under 20 (assuming it's not a valid age):
    ```sql
    DELETE FROM employees WHERE age < 20;

    ```
