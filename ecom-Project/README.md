# 🛒 E-Commerce Backend

A robust and scalable **Spring Boot RESTful backend** for an e-commerce application, designed to efficiently manage products, inventory, and database operations. The project follows a clean layered architecture and leverages **Spring Boot**, **Spring Data JPA**, and **H2 Database** to provide a lightweight yet production-ready backend solution.

The application exposes REST APIs for product management and demonstrates modern backend development practices, including dependency injection, ORM-based database interaction, Maven-based build management, and developer-friendly tooling for rapid development.

---

# 📖 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Project Workflow](#project-workflow)
- [Database Design](#database-design)
- [Project Structure](#project-structure)
- [Development Environment](#development-environment)
- [REST API Overview](#rest-api-overview)
- [Future Improvements](#future-improvements)

---

# 📌 Overview

The **E-Commerce Backend** is a RESTful web application built using **Spring Boot 4**, designed to serve as the backend for an online shopping platform.

It provides APIs for managing products and inventory while demonstrating enterprise backend development concepts such as:

- REST API development
- Layered architecture
- ORM using Hibernate
- CRUD operations
- Dependency Injection
- Maven project management
- H2 in-memory database
- Spring Boot DevTools
- Lombok integration

The project is lightweight, modular, and easy to extend for larger e-commerce systems.

---

# ✨ Features

## 📦 Product Management

The application allows complete management of product information.

Supported operations include:

- Add new products
- Retrieve all products
- Retrieve product by ID
- Update existing products
- Delete products

Each product stores essential information such as:

- Product Name
- Description
- Brand
- Category
- Price
- Quantity
- Release Date

---

## 🗄️ Inventory Management

Every product maintains an inventory count.

The backend stores product quantity and enables inventory tracking for future stock management features.

---

## 🔄 RESTful APIs

The project exposes REST APIs following standard HTTP methods.

Supported operations include:

- GET
- POST
- PUT
- DELETE

The APIs are stateless and can easily integrate with frontend applications such as React, Angular, or mobile applications.

---

## ⚡ ORM with Spring Data JPA

Database interaction is handled using **Spring Data JPA** together with **Hibernate**.

Instead of writing SQL for every operation, repositories provide built-in CRUD methods, making development faster and cleaner.

Benefits include:

- Automatic SQL generation
- Entity mapping
- Reduced boilerplate code
- Easy database integration

---

## 💾 H2 In-Memory Database

The project uses an **H2 in-memory database** for development and testing.

Advantages include:

- No external database installation required
- Fast startup
- Lightweight
- Easy testing
- Automatic database creation during runtime

The H2 Console is also enabled for inspecting tables and executing SQL queries directly through the browser.

---

## 🔥 Developer Productivity

Several tools have been integrated to improve the development experience:

- Spring Boot DevTools
- Lombok
- Maven Wrapper
- H2 Console

These tools significantly reduce development time and simplify project maintenance.

---

# 🏗️ Architecture

The project follows the **Controller-Service-Repository** architecture.

```
                Client
                   │
                   ▼
          REST Controller Layer
                   │
                   ▼
            Service Layer
        (Business Logic)
                   │
                   ▼
      Repository (Spring Data JPA)
                   │
                   ▼
            H2 Database
```

Each layer has a dedicated responsibility, making the project modular and easy to maintain.

---

## Controller Layer

Responsibilities:

- Handles incoming HTTP requests
- Maps REST endpoints
- Returns JSON responses
- Performs request validation

---

## Service Layer

The Service Layer contains the application's business logic.

Responsibilities include:

- Product validation
- Inventory management
- CRUD operations
- Exception handling

---

## Repository Layer

The Repository Layer communicates directly with the database using Spring Data JPA.

Responsibilities include:

- CRUD operations
- Entity persistence
- Query execution
- Data retrieval

Hibernate automatically translates repository operations into SQL queries.

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| Java 17 | Programming Language |
| Spring Boot 4.1 | Backend Framework |
| Spring Web MVC | REST API Development |
| Spring Data JPA | ORM & Database Access |
| Hibernate | Object Relational Mapping |
| H2 Database | In-Memory Database |
| Maven | Build Automation |
| Lombok | Boilerplate Code Reduction |
| Spring Boot DevTools | Hot Reload |
| Maven Wrapper | Cross-platform Build |

---

# 🔄 Project Workflow

```
Client
   │
   ▼
REST API Request
   │
   ▼
Controller
   │
   ▼
Service Layer
   │
   ▼
Repository
   │
   ▼
H2 Database
   │
   ▼
JSON Response
```

---

# 🗄️ Database Design

The project maintains a **Product** entity with the following attributes.

| Field | Type | Description |
|--------|------|-------------|
| id | Integer | Primary Key (Auto Increment) |
| name | String | Product Name |
| desc | String | Product Description |
| brand | String | Product Brand |
| category | String | Product Category |
| price | Decimal | Product Price |
| quantity | Integer | Available Stock |
| releaseDate | Date | Product Release Date |

The database schema is automatically managed using Hibernate.

---

# 📂 Project Structure

```
ecom-project
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── BedantaM
│   │   │           └── ecom_Project
│   │   │               ├── controller
│   │   │               ├── service
│   │   │               ├── repository
│   │   │               ├── model
│   │   │               └── EcomProjectApplication.java
│   │   │
│   │   └── resources
│   │       ├── application.properties
│   │       └── data.sql
│   │
│   └── test
│
├── pom.xml
├── mvnw
├── mvnw.cmd
├── .gitignore
├── .gitattributes
└── README.md
```

---

# ⚙️ Development Environment

The project includes several developer-friendly tools.

### Maven Wrapper

The project contains:

- `mvnw`
- `mvnw.cmd`

These scripts allow the project to be built without installing Maven globally.

---

### Lombok

Lombok automatically generates:

- Getters
- Setters
- Constructors
- `toString()`
- `equals()`
- `hashCode()`

This keeps the code clean and reduces boilerplate.

---

### Spring Boot DevTools

DevTools improves development by providing:

- Automatic restart
- Faster application reload
- Improved developer productivity

---

### H2 Console

The integrated H2 Console allows developers to:

- Inspect database tables
- Execute SQL queries
- Verify inserted data
- Debug database operations

---

### Version Control

The project includes:

**.gitignore**

Excludes:

- `target/`
- `build/`
- IDE-specific files
- Log files

**.gitattributes**

Ensures consistent line endings across operating systems:

- `LF` for Linux/macOS
- `CRLF` for Windows batch files

This prevents cross-platform compatibility issues.

---

# 📡 REST API Overview

| Method | Endpoint | Description |
|----------|----------|-------------|
| GET | `/products` | Retrieve all products |
| GET | `/products/{id}` | Retrieve product by ID |
| POST | `/products` | Add a new product |
| PUT | `/products/{id}` | Update an existing product |
| DELETE | `/products/{id}` | Delete a product |

> **Note:** Replace endpoint paths with your actual controller mappings if they differ.

---

# 🚀 Future Improvements

The project can be extended with several enterprise-level features:

- User Authentication using Spring Security
- JWT-based Authorization
- Role-Based Access Control
- Shopping Cart Module
- Order Management
- Payment Gateway Integration
- Product Search & Filtering
- Product Image Upload
- Pagination & Sorting
- Wishlist
- Review & Rating System
- Docker Containerization
- PostgreSQL/MySQL Support
- Redis Caching
- Swagger/OpenAPI Documentation
- Unit & Integration Testing
- CI/CD Pipeline using GitHub Actions

---

# 🎯 Learning Outcomes

This project demonstrates practical knowledge of:

- Spring Boot Application Development
- REST API Design
- Java Backend Development
- Spring MVC
- Spring Data JPA
- Hibernate ORM
- H2 Database
- Maven Build System
- Layered Architecture
- Dependency Injection
- CRUD Operations
- Lombok Integration
- Spring Boot DevTools
- Enterprise Backend Development Practices

---

# 👨‍💻 Author

**Bedanta Mahanty**

If you found this project useful, consider ⭐ starring the repository and feel free to contribute by opening issues or pull requests.
