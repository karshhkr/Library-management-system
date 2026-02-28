# 📚 Library Management System

A secure, role-based **Library Management System** built using **Java, Spring Boot, Spring Security, MySQL, Hibernate, and Thymeleaf**.

This project demonstrates backend development skills including authentication, authorization, layered architecture, business logic implementation, and database integration.

---

## 🚀 Project Overview

The system allows administrators to manage books and students, issue and return books, and track overdue records.  
Users can securely log in and access features based on their assigned roles.

---

## ✨ Key Features

### 🔐 Authentication & Authorization
- Role-based access control (ADMIN / USER)
- Spring Security integration
- Custom `UserDetailsService`
- BCrypt password hashing
- Account enable/disable handling
- Method-level security using `@PreAuthorize`

### 📖 Book Management
- Add, edit, delete books (ADMIN only)
- View book list (All authenticated users)

### 🎓 Student Management
- Add, edit, delete students (ADMIN only)
- View student list (All authenticated users)

### 🔄 Issue & Return System
- Issue books to students
- Return books
- Track issue and due dates
- Overdue detection logic

### 🔔 Notification System
- Store notifications per student
- Display latest notifications first
- Integrated with overdue tracking

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Java 24 |
| Framework | Spring Boot 4 |
| Security | Spring Security 7 |
| Database | MySQL 8 |
| ORM | Hibernate (JPA) |
| Template Engine | Thymeleaf |
| Build Tool | Maven |
| Server | Embedded Tomcat |

---

## 🏗 Architecture

The project follows a clean layered architecture:

```
Controller → Service → Repository → Database
```

### Layer Breakdown

- **Entity Layer** – JPA entities mapped to database tables  
- **Repository Layer** – Interfaces extending `JpaRepository`  
- **Service Layer** – Business logic implementation  
- **Controller Layer** – Handles HTTP requests  
- **Security Configuration** – Role-based access management  

---

## 🧠 Backend Concepts Implemented

- Layered architecture design
- Spring Security configuration
- Role-based endpoint protection
- Method-level authorization
- Password encryption using BCrypt
- Custom authentication logic
- JPA entity relationships
- Overdue calculation logic
- Notification management system

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/library-management-system.git
cd library-management-system
```

---

### 2️⃣ Create Database

```sql
CREATE DATABASE library_db;
```

---

### 3️⃣ Configure `application.properties`

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/library_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

---

### 4️⃣ Run Application

```bash
mvn clean install
mvn spring-boot:run
```

Open in browser:

```
http://localhost:8080
```

---

## 🔒 User Roles & Permissions

| Role | Permissions |
|------|------------|
| ADMIN | Full CRUD access (Books, Students, Issues) |
| USER | View-only access |

---

## 📂 Project Structure

```
src
 └── main
     ├── java
     │   └── com.example.Library_management_system
     │       ├── controller
     │       ├── service
     │       ├── repository
     │       ├── entity
     │       └── config
     └── resources
         ├── templates
         ├── static
         └── application.properties
```

---

## 📈 Future Improvements

- Pagination support
- REST API version with JWT authentication
- Swagger API documentation
- Docker containerization
- Fine calculation automation
- Cloud deployment (AWS / Render / Railway)

---

## 👨‍💻 Author

**Utkarsh Kumar Dabgarwal**  
Java Backend Developer  
Spring Boot | Security | REST APIs | MySQL  

---

## 📌 License

This project is created for educational and demonstration purposes.
