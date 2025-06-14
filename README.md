# Employee Management System (Java Swing + JDBC)
Project Description
The Employee Management System is a desktop-based Java application built using Java Swing for the graphical user interface (GUI) and JDBC (Java Database Connectivity) for database operations. It allows users to perform CRUD (Create, Read, Update, Delete) operations on employee records stored in a PostgreSQL database.

Key Features:
              *Employee Record Management
              *Add new employees with details (ID, Name, Address, Salary, Age, Date of Birth)
              *View all employees in a scrollable table
              *Edit existing employee details
              *Delete employee records with confirmation

 Database Integration:
              *PostgreSQL backend for data persistence
              *JDBC for secure database connectivity
              *Prepared statements to prevent SQL injection

 User-Friendly GUI
              *Swing-based interface with intuitive controls
              *Input validation for data integrity
              *Confirmation dialogs for critical actions (e.g., deletion)

Error Handling
              *Displays meaningful error messages for database issues
              *Validates input fields (e.g., numeric checks for salary/age)
              *Technologies Used
Frontend: Java Swing (GUI)
              *Backend: JDBC (Java Database Connectivity)

Database: PostgreSQL

Build Tool: Maven/Gradle (optional)

Who Can Use This?
                *HR Departments – Manage employee records efficiently
                *Small Businesses – Track staff details without complex software
                *Java Learners – Understand Swing + JDBC integration
Developers – Extend with new features (e.g., search, export to Excel)

How It Works

                *Connect to PostgreSQL: The app establishes a secure connection to the database.
Display Records: Employee data is fetched and shown in a table.

CRUD Operations:

Create: Add new employees via a dialog form.

Read: View all records in a scrollable table.

Update: Modify employee details (name, salary, etc.).

Delete: Remove employees with a confirmation prompt.
Create table like this-
      DataBase SetUp
      CREATE DATABASE employeedb;
      CREATE TABLE Employees 
      (
          id INT PRIMARY KEY,
          name VARCHAR(100) NOT NULL,
          address VARCHAR(200),
          salary DECIMAL(10,2),
          age INT,
          dob DATE
      );

Configuration:
Edit the database connection settings in src/main/java/controller/projrct_name.java
  *private static final String DB_URL = "jdbc:postgresql://localhost:5432/employeedb";
  *private static final String DB_USER = "your_username";
  *private static final String DB_PASSWORD = "your_password";

Project Structure:
src/
├── main/
│   ├── java/
│   │   ├── controller/    # Application logic
│   │   │   └── JDBC2.java
│   │   ├── model/         # Data structures
│   │   │   └── Employee.java
│   │   └── view/          # UI components
│   │       └── EmployeeTableModel.java
│   └── resources/         # Configuration files
├── screenshots/           # Application screenshots
postgresql-42.7.3.jar      # JDBC driver

Dependencies:
  *PostgreSQL JDBC Driver (Download)
  *Java Swing (Included in JDK)

Suggested Improvements (For Future Development):
  * Add login authentication
  * Implement search/filter functionality
  * Add export to CSV/PDF
  *Include unit tests
  *Dockerize the application
