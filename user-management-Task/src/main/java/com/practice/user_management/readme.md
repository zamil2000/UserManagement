# User Management System

This project is a Spring Boot-based User Management System that provides user registration, authentication, and administrative functionalities. It includes security features such as Basic Authentication, IP tracking, Swagger documentation, JUnit test cases, and Dockerization for easy deployment.

## Features

1. **User Registration**: Allows users to register with Name, Email, Gender, and Password.
2. **Unique Email Validation**: Ensures no duplicate email registration.
3. **IP Address & Country Tracking**: Stores user's IP address and country details using [ipify](https://www.ipify.org/) and [ip-api](https://ip-api.com/).
4. **User Authentication**: API to validate users with Email and Password.
5. **Basic Authentication Security**: Protects API endpoints with authentication.
6. **Admin Privileges**:
   - View all registered users.
   - Delete a user by email.
7. **JUnit Test Cases**: Service layer tested using JUnit.
8. **Swagger Documentation**: API testing and documentation.
9. **Dockerized Application**: Supports containerized deployment.

## API Endpoints

### 1. User Registration
**Endpoint:** `POST /api/users/register`
**Description:** Registers a new user.

### 2. Health Check
**Endpoint:** `GET /api/users/health`
**Description:** Checks if the service is running.

### 3. User Authentication
**Endpoint:** `GET /api/users/authenticate`
**Description:** Authenticates a user by email and password.

### 4. Get All Users (Admin Only)
**Endpoint:** `GET /api/users/all`
**Description:** Retrieves all registered users (Admin access required).

**Admin Details:**
Username :admin
Password : admin123 .

provide username and password in Authorization and select type "Basic Auth" in Postman


### 5. Delete User (Admin Only)
**Endpoint:** `DELETE /api/users/delete`
**Description:** Deletes a user by email (Admin access required).

**Admin Details:**
Username :admin
Password : admin123 .

provide username and password in Authorization and select type "Basic Auth" in Postman

## Running the Application

### Prerequisites
- Java 17+
- Maven
- Docker

### Build and Run Locally
```sh
mvn clean install
mvn spring-boot:run
```

### Build and Run with Docker
```sh
docker build -t user-management-task .
docker run -p 8080:8080 user-management-task
```

## Testing
- Use **Postman** or **Swagger UI** to test the APIs.
- Swagger UI: `http://localhost:8080/swagger-ui.html`
- Run JUnit tests using:
  ```sh
  mvn test
  ```

## Deployment
1. Build the application with Maven.
2. Create a Docker image and run it.
3. Expose the API for usage.



