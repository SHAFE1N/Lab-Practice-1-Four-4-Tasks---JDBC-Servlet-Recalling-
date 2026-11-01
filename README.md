# Java Lab Assignment — November 1, 2026

**Department:** Information and Communication Technology (ICT)  
**University:** Mawlana Bhashani Science and Technology University (MBSTU)  
**Student Name:** Shahrier Mokammel Shafeen  
**Student ID:** IT24050

---

## Task 1: Installation of IntelliJ IDEA Ultimate

### Objective

Install and configure IntelliJ IDEA Ultimate as the Integrated Development Environment (IDE) for Java application development.

### Software and Tools

- IntelliJ IDEA Ultimate 2026.2
- Java Development Kit (OpenJDK 26)
- Apache Maven
- Windows Operating System

### Procedure

1. Downloaded and installed IntelliJ IDEA Ultimate.
2. Activated IntelliJ IDEA Ultimate using the JetBrains educational license.
3. Configured OpenJDK 26 as the Java SDK.
4. Created a Maven-based Java project.
5. Verified the IDE configuration by compiling and executing Java code.

### Installation Screenshot

![IntelliJ IDEA Ultimate Installation](Task_1_IntelliJ/Install IntelliJ IDEA Ultimate/Screenshot 2026-11-01 105844.png)


### Result

IntelliJ IDEA Ultimate was successfully installed, activated, and configured for Java development.

---

## Task 2: JDBC Database Connectivity — N-th Prime Number Insertion

**Marks: 05**

### Objective

Develop a Java application that calculates the n-th prime number, establishes a JDBC connection with MySQL, inserts the calculated prime number into a database table, and retrieves the stored record for verification.

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

### Database Table Structure

| Column | Data Type | Description |
|---|---|---|
| id | INT | Auto-increment primary key |
| n | INT | Position of the prime number |
| prime_number | INT | Calculated n-th prime number |

### SQL Table Creation

```sql
CREATE DATABASE IF NOT EXISTS jdbc_lab;

CREATE TABLE IF NOT EXISTS jdbc_lab.shafeen_shahrier_prime (
    id INT AUTO_INCREMENT PRIMARY KEY,
    n INT NOT NULL,
    prime_number INT NOT NULL
);
```

### Program Implementation

The Java application performs the following operations:

1. Takes an integer `n` as input.
2. Calculates the n-th prime number using a primality-checking function.
3. Establishes a JDBC connection to the MySQL database.
4. Inserts the calculated prime number using `PreparedStatement`.
5. Retrieves the inserted record using its generated ID.
6. Displays the stored information in the console.

**Source Code:** [Main.java](Task_2_JDBC/Main.java)

**Maven Configuration:** [pom.xml](Task_2_JDBC/pom.xml)

**SQL Script:** [database.sql](Task_2_JDBC/database.sql)

### Sample Input

```text
10
```

### Sample Output

```text
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

The following screenshot demonstrates successful JDBC connectivity, n-th prime number calculation, database insertion, and record retrieval.

![Java JDBC Prime Number Execution](Task_2_JDBC/screenshots/java_output.png)

### MySQL Database Verification

The following record was successfully retrieved from the MySQL database:

| id | n | prime_number |
|---|---|---|
| 1 | 10 | 29 |

### MySQL Database Screenshot

The following screenshot shows the inserted record in the `shafeen_shahrier_prime` table.

![MySQL Prime Number Database Output](Task_2_JDBC/screenshots/mysql_output.png)

### Result Analysis

The program successfully calculated the 10th prime number as **29**. JDBC connectivity was established using MySQL Connector/J, and the calculated value was inserted into the database.

The stored record was retrieved successfully using a SQL SELECT statement, confirming correct database insertion and retrieval.

### Conclusion

The experiment successfully demonstrated Java Database Connectivity (JDBC), prime number calculation, parameterized SQL insertion, and database record retrieval using Java and MySQL.

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
