# Java Lab Practice — November 1, 2026

## JDBC & Servlet Lab Assignment

**Student Name:** Shahrier Mokammel Shafeen  
**Student ID:** IT24050 
**Department:** Information and Communication Technology (ICT)  
**University:** Mawlana Bhashani Science and Technology University (MBSTU)  
**IDE:** IntelliJ IDEA Ultimate  
**Programming Language:** Java 26

---

## Task 1: Install IntelliJ IDEA Ultimate

**Status: Completed**

### Objective

To install, activate, and configure IntelliJ IDEA Ultimate for Java application development.

### Software Requirements

- IntelliJ IDEA Ultimate 2026.2
- OpenJDK 26
- Apache Maven
- Windows 11

### Implementation Procedure

1. Downloaded IntelliJ IDEA Ultimate from the JetBrains website.
2. Installed and activated IntelliJ IDEA Ultimate using an educational license.
3. Configured Java Development Kit (OpenJDK 26).
4. Created a Maven-based Java project.
5. Successfully configured the IDE for Java development.

### Installation Screenshot

![IntelliJ IDEA Ultimate Installation](Install%20IntelliJ%20IDEA%20Ultimate/Screenshot%202026-11-01%20105844.png)

### Result

IntelliJ IDEA Ultimate was successfully installed, activated, and configured for Java development.

---

## Task 2: JDBC Database Connectivity — Prime Number Insertion

**Score: 05**  
**Status: Completed**

### Objective

To establish JDBC connectivity between Java and MySQL, calculate the n-th prime number, insert it into a database table, and retrieve the stored record to verify successful insertion.

### Technologies Used

- Java 26
- IntelliJ IDEA Ultimate
- MySQL Server 8.4
- MySQL Connector/J 9.4.0
- JDBC API
- Apache Maven

### Database Information

**Database Name:** `jdbc_lab`  
**Table Name:** `shafeen_shahrier_prime`

### Database Table Creation

```sql id="6p5t4s"
CREATE DATABASE IF NOT EXISTS jdbc_lab;

CREATE TABLE IF NOT EXISTS jdbc_lab.shafeen_shahrier_prime (
    id INT AUTO_INCREMENT PRIMARY KEY,
    n INT NOT NULL,
    prime_number INT NOT NULL
);
```

### Table Structure

| Column | Data Type | Description |
|---|---|---|
| id | INT | Auto-increment primary key |
| n | INT | Position of the prime number |
| prime_number | INT | Calculated n-th prime number |

### Algorithm

1. Read a positive integer `n` from the user.
2. Check successive integers to identify prime numbers.
3. Continue counting until the n-th prime number is found.
4. Establish a JDBC connection with MySQL.
5. Insert `n` and the calculated prime number using `PreparedStatement`.
6. Retrieve the stored record using its generated ID.
7. Display the retrieved record in the Java console.

### Java Program Description

The application contains two main methods:

- `isPrime(int num)` — Checks whether a number is prime.
- `nthPrime(int n)` — Finds the n-th prime number.

The application uses `DriverManager`, `Connection`, `PreparedStatement`, and `ResultSet` for database operations.

### Sample Input

```text id="cb2oq1"
10
```

### Sample Output

```text id="0xky9u"
Enter n: 10
10-th prime number: 29
Connected to MySQL successfully!
Prime inserted successfully!
Auto-commit: true

Stored Record:
ID: 1
n: 10
Prime: 29
```

### Java Execution Screenshot

The following screenshot demonstrates successful prime number calculation, JDBC connection, database insertion, and record retrieval.

![Java JDBC Execution Screenshot](JDBC%20Database%20Connectivity%20%E2%80%93%20Prime%20Number%20Insertion/Java_output_screenshot.png)

### Database Verification

The inserted record was verified using the SQL query:

```sql id="ylwqhk"
SELECT * FROM jdbc_lab.shafeen_shahrier_prime;
```

**Verified Record:**

| id | n | prime_number |
|---|---|---|
| 1 | 10 | 29 |

### MySQL Database Screenshot

The following screenshot shows the stored record in the MySQL database table.

![MySQL Database Record](JDBC%20Database%20Connectivity%20%E2%80%93%20Prime%20Number%20Insertion/Database_record.png)

### Result Analysis

The Java application successfully calculated the 10th prime number as **29**.

JDBC connectivity was established with MySQL Server using MySQL Connector/J. The calculated prime number was inserted into the `shafeen_shahrier_prime` table and retrieved successfully.

The database screenshot confirms that the inserted record was stored correctly.

### Conclusion

The experiment successfully demonstrated Java Database Connectivity (JDBC), prime number calculation, SQL insertion using prepared statements, and record retrieval from a relational database.

---

## Assignment Progress

| Task | Description | Status |
|---|---|---|
| Task 1 | IntelliJ IDEA Ultimate Installation | Completed |
| Task 2 | JDBC N-th Prime Number Insertion | Completed |
| Task 3 | Apache Tomcat and HelloWorld Servlet | Pending |
| Task 4 | Browser-Based Prime Number Checker Servlet | Pending |

---

**Submitted By:** Shahrier Mokammel Shafeen  
**Department of ICT, MBSTU**
