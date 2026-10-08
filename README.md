# Employee Management System

A simple **Employee Management System** built using **Java and Spring Boot** that provides REST APIs to manage employee records. The application performs CRUD operations and stores employee data in a **MySQL database** using **JPA/Hibernate**.

## Features

* Add a new employee
* View all employees
* Search employees
* Update employee details
* Delete an employee
* Persistent storage using MySQL
* Database interaction using JPA/Hibernate
* RESTful APIs for employee management

## Technologies Used

* **Java**
* **Spring Boot**
* **Spring Data JPA**
* **Hibernate**
* **MySQL**
* **Maven**
* **REST API**

## API Operations

| Method | Endpoint          | Description                  |
| ------ | ----------------- | ---------------------------- |
| POST   | `/employees`      | Add a new employee           |
| GET    | `/employees`      | Get all employees            |
| GET    | `/employees/{id}` | Search/Get an employee by ID |
| PUT    | `/employees/{id}` | Update employee details      |
| DELETE | `/employees/{id}` | Delete an employee           |

## Database

The application uses **MySQL** for storing employee information.

**Spring Data JPA** is used to interact with the database, while **Hibernate** acts as the JPA implementation responsible for mapping Java objects to database tables.

This project helped me understand:

* Connecting a Spring Boot application with MySQL
* Creating entities using JPA annotations
* Object-Relational Mapping (ORM)
* Using repositories for database operations
* Performing CRUD operations through JPA
* How Hibernate handles persistence between Java objects and database records

## Project Structure

```text
src
└── main
    ├── java
    │   └── ... 
    │       ├── controller
    │       ├── service
    │       ├── repository
    │       └── entity
    │
    └── resources
        └── application.properties
```

## How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Open the project

Open the project in **IntelliJ IDEA** or any preferred Java IDE.

### 3. Configure MySQL

Create a MySQL database and update the database configuration in:

```text
src/main/resources/application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 4. Run the application

Run the Spring Boot application from the main application class.

The application will start on:

```text
http://localhost:8080
```

## Example API Requests

### Add Employee

```http
POST /employees
```

Example request body:

```json
{
  "name": "John",
  "email": "john@example.com",
  "department": "IT"
}
```

### Get All Employees

```http
GET /employees
```

### Get Employee by ID

```http
GET /employees/1
```

### Update Employee

```http
PUT /employees/1
```

### Delete Employee

```http
DELETE /employees/1
```

## What I Learned

This project was an important step in my Spring Boot learning journey. Compared with my previous project, this project introduced **database connectivity and persistence**.

Through this project, I gained practical understanding of:

* Spring Boot REST APIs
* CRUD operations
* MySQL database integration
* JPA and Hibernate
* Entity and repository concepts
* ORM and persistence
* Connecting the application layer with a relational database

## Future Enhancements

* Add input validation
* Add exception handling
* Add pagination and sorting
* Add search by different employee fields
* Add authentication and authorization
