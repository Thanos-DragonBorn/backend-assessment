
---

### `backend-java/README.md`

```markdown
# Spring Boot Backend Service - Java Exercise

This exercise is designed for Java proficient applicants to build a Spring Boot application that demonstrates your ability to create a RESTful API, integrate with an in-memory database, return appropriate HTTP response codes, and secure your endpoints with Spring Security.

## Requirements

1. **REST API Endpoints:**
   - **GET `/items`**: Retrieve a list of items.
   - **GET `/items/{id}`**: Retrieve a specific item by its unique ID.
   - **POST `/items`**: Create a new item.
   - **PUT `/items/{id}`**: Update an existing item.
   - **DELETE `/items/{id}`**: Delete an item.

2. **Database Integration:**
   - Use an H2 in-memory database for data persistence.
   - Seed the database with initial sample data so that GET requests return sample items.

3. **HTTP Response Codes:**
   - Ensure that each endpoint returns appropriate HTTP response codes (e.g., 200 OK, 201 Created, 400 Bad Request, 404 Not Found, etc.).

4. **Security:**
   - Secure your API endpoints using Spring Security.
   - Implement basic authentication using an in-memory user store.
   - Only authenticated users should be able to access the API endpoints.

5. **Build & Run:**
   - Use Maven or Gradle as your build tool.
   - Provide instructions on how to build and run your application (e.g., using `mvn spring-boot:run`).

## Bonus (Optional)
- Implement role-based access control.
- Write unit tests for your API endpoints.

## Starter Code (Optional)

Below is a minimal example of a Spring Boot application to help you get started:

```java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {
   public static void main(String[] args) {
       SpringApplication.run(DemoApplication.class, args);
   }
}

## You can use Spring Initializr to bootstrap your project with the following dependencies:
- Spring Web
- Spring Data JPA
- H2 Database
- Spring Security

## Submission Guidelines
- Place your solution within this repository.
- Update this README with instructions on how to build, run, and test your application.
- Ensure your code is clean, well-organized, and well-documented.

Good luck!