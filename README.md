# Product Service - Spring Boot Microservice

[![Java](https://img.shields.io/badge/Java-17+-orange.svg)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![H2 Database](https://img.shields.io/badge/Database-H2-blue.svg)](https://www.h2database.com/)
[![Swagger](https://img.shields.io/badge/API%20Docs-Swagger-85EA2D.svg)](https://swagger.io/)

A RESTful microservice built with Spring Boot for managing products, featuring an in-memory H2 database and Swagger API documentation.

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Database Access](#database-access)
- [API Documentation](#api-documentation)
- [Project Structure](#project-structure)
- [Testing the APIs](#testing-the-apis)
- [Lab Information](#lab-information)

## 🎯 About the Project

This project is a simple Product Management microservice developed as part of the **SLIIT DevOps Lab 3** assignment. It demonstrates the implementation of a RESTful API using Spring Boot with CRUD operations, in-memory database persistence, and automated API documentation.

## ✨ Features

- ✅ **CRUD Operations**: Create, Read, Update, and Delete products
- ✅ **In-Memory Database**: H2 database for runtime data persistence
- ✅ **RESTful API**: Well-structured REST endpoints
- ✅ **API Documentation**: Auto-generated Swagger UI documentation
- ✅ **JPA Integration**: Spring Data JPA for database operations
- ✅ **H2 Console**: Web-based database console for debugging

## 🛠️ Technologies Used

| Technology | Version | Purpose |
|------------|---------|---------|
| **Java** | 17+ | Programming Language |
| **Spring Boot** | 3.x | Application Framework |
| **Spring Web** | - | REST API Development |
| **Spring Data JPA** | - | Database Operations |
| **H2 Database** | - | In-Memory Database |
| **Springdoc OpenAPI** | - | API Documentation (Swagger) |
| **Maven** | - | Build Tool |

## 🚀 Getting Started

### Prerequisites

Before running this application, ensure you have the following installed:

- **Java Development Kit (JDK)** 17 or higher
- **Maven** 3.6+ (or use the Maven wrapper included)
- **IDE** (IntelliJ IDEA, Eclipse, or VS Code recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Ridma-Sathsara/Lab-3-CSTE.git
   cd Lab-3-CSTE
   ```

2. **Build the project**
   ```bash
   mvn clean install
   ```

### Running the Application

You can run the application using Maven or your IDE:

**Using Maven:**
```bash
mvn spring-boot:run
```

**Using Java:**
```bash
java -jar target/product-service-0.0.1-SNAPSHOT.jar
```

The application will start on **http://localhost:8080**

## 📡 API Endpoints

### Product Management

| Method | Endpoint | Description | Request Body |
|--------|----------|-------------|--------------|
| `POST` | `/products` | Create a new product | `{"name": "Product Name", "price": 99.99}` |
| `GET` | `/products` | Get all products | - |
| `GET` | `/products/{id}` | Get product by ID | - |
| `DELETE` | `/products/{id}` | Delete a product | - |

### Example Requests

**Create a Product:**
```bash
curl -X POST http://localhost:8080/products \
  -H "Content-Type: application/json" \
  -d '{"name": "Laptop", "price": 1299.99}'
```

**Get All Products:**
```bash
curl http://localhost:8080/products
```

**Get Product by ID:**
```bash
curl http://localhost:8080/products/1
```

**Delete a Product:**
```bash
curl -X DELETE http://localhost:8080/products/1
```

## 🗄️ Database Access

### H2 Console

Access the H2 database console at: **http://localhost:8080/h2-console**

**Connection Details:**
- **JDBC URL:** `jdbc:h2:mem:testdb`
- **Username:** `sa`
- **Password:** `password`
- **Driver Class:** `org.h2.Driver`

The H2 console allows you to:
- View the `PRODUCT` table structure
- Execute SQL queries
- Monitor database state during runtime

## 📚 API Documentation

### Swagger UI

Interactive API documentation is available at: **http://localhost:8080/swagger-ui.html**

Swagger UI provides:
- Complete API endpoint listing
- Request/response schemas
- Interactive API testing interface
- Model definitions

### OpenAPI Specification

Raw OpenAPI JSON specification: **http://localhost:8080/v3/api-docs**

## 📁 Project Structure

```
Lab-3-CSTE/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/
│       │       └── sliit/
│       │           └── product_service/
│       │               ├── ProductServiceApplication.java    # Main application class
│       │               ├── controller/
│       │               │   └── ProductController.java        # REST controller
│       │               ├── model/
│       │               │   └── Product.java                  # Product entity
│       │               └── repository/
│       │                   └── ProductRepository.java        # JPA repository
│       └── resources/
│           └── application.properties                        # Application configuration
├── target/                                                   # Compiled classes
├── pom.xml                                                   # Maven configuration
└── README.md                                                 # This file
```

## 🧪 Testing the APIs

### Using Swagger UI (Recommended)

1. Navigate to http://localhost:8080/swagger-ui.html
2. Expand the endpoint you want to test
3. Click "Try it out"
4. Enter the required parameters
5. Click "Execute"

### Using Postman

1. Import the OpenAPI specification from http://localhost:8080/v3/api-docs
2. Test each endpoint with sample data

### Using cURL

See the [API Endpoints](#api-endpoints) section for cURL examples.

## 📖 Lab Information

**Module:** Current Trends in Software Engineering (SE4010)  
**Lab:** DevOps Lab 3  
**Topic:** Building a Spring Boot Microservice with In-Memory Database & Swagger  
**Institution:** SLIIT - Faculty of Computing  
**Department:** Computer Science & Software Engineering  
**Academic Year:** 2025 | Semester 1

### Lab Objectives

- ✅ Create a RESTful microservice using Spring Boot
- ✅ Implement CRUD operations with REST endpoints
- ✅ Use H2 in-memory database for data persistence
- ✅ Document APIs using Swagger/OpenAPI

## 👨‍💻 Author

**[Your Name]**  
IT Number: [Your IT Number]  
SLIIT - Faculty of Computing

## 📝 License

This project is created for educational purposes as part of the SLIIT DevOps Lab curriculum.

---

**Happy Coding! 🚀**
