# Product and Category Management API

This project is a Spring Boot application for managing products and categories. It provides a REST API with CRUD operations for `Category` and `Product` entities and supports pagination, with a one-to-many relationship between `Category` and `Product`.

## Requirements

The following requirements were implemented:

- **Spring Boot** for application setup and execution.
- **REST Controller** for API endpoints.
- **Relational Database (RDB)** configuration (instead of in-memory databases).
- **Annotation-based configuration** (avoiding XML).
- **JPA & Hibernate** for ORM and database interactions.

## Features

1. **Category CRUD Operations**
   - API endpoints to create, retrieve, update, and delete categories.
   - Pagination support for listing categories.

2. **Product CRUD Operations**
   - API endpoints to create, retrieve, update, and delete products.
   - Pagination support for listing products.
   - One-to-many relationship between `Category` and `Product`.

3. **Server-Side Pagination**
   - Supports pagination for category and product listing endpoints.

4. **Relationship Between Categories and Products**
   - Each category can have multiple products (one-to-many relationship).
   - While fetching a single product, its associated category details are included in the response.

## Technologies Used

- Java 8+
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL (or other RDBs as configured)
- Maven

## Setup Instructions

### Prerequisites

1. **Java**: Ensure Java 8 or above is installed.
2. **Maven**: Make sure Maven is installed.
3. **Database**: Configure a relational database (e.g., MySQL) for the application.

### Database Configuration

Configure your database connection in `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
