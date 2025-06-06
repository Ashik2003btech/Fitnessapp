# FitnessApp

A simple Java console application to manage fitness users with CRUD operations using JDBC and MySQL.

---

## Project Overview

FitnessApp allows users to insert, update, delete, and find fitness users with personal details such as name, age, contact, gender, height, and weight. It calculates BMI (Body Mass Index) and provides BMI categories using business logic encapsulated in a service layer.

The project follows a layered architecture with separate packages for:

- **model:** User entity class with getters/setters.
- **dao:** Data Access Object interface and implementation for database CRUD.
- **exception:** Custom exception handling.
- **service:** Business logic like BMI calculation.
- **main:** Console-based user interface (CUI) to interact with the application.

---

## Features

- Insert new users into MySQL database.
- Fetch user details by ID.
- List all users.
- Update user details.
- Delete user records.
- Calculate and categorize BMI.

---

## Technologies Used

- Java 17 (or your JDK version)
- JDBC for database connectivity
- MySQL for backend database
- Console user interface

---

## Database Setup

Make sure you have MySQL installed and create a database named `fitness` with the following `user_data` table:

```sql
CREATE TABLE user_data (
  user_id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  age INT,
  contact VARCHAR(50),
  gender_id INT,
  height_cm DOUBLE,
  weight_kg DOUBLE
);


git clone https://github.com/yourusername/FitnessApp.git


com.fitnessapp
├── dao
│   ├── IUserDAO.java
│   └── UserDAO.java
├── exception
│   └── UserNotFoundException.java
├── main
│   └── FitnessApp.java
├── model
│   └── User.java
└── service
    └── FitnessService.java

1. Insert User
2. Find User by ID
3. List All Users
4. Update User
5. Delete User
6. Exit
Choose an option: 1
Name: John Doe
Age: 30
Contact: 1234567890
Gender ID: 1
Height (cm): 175
Weight (kg): 70
Inserted user with ID: 1

---
