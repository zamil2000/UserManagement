# User Management System

A Spring Boot-based User Management System with user registration, authentication, and admin functionalities. The system includes security features like Basic Authentication, IP tracking, and Swagger documentation.

## Features

- User registration with name, email, gender, and password
- Unique email validation to prevent duplicate registrations
- IP address and country tracking
- Basic Authentication for security
- Admin functionalities (view all users, delete users)
- JUnit test coverage for service layer
- Swagger API documentation
- Docker support

## API Endpoints

### Public Endpoints

1. **User Registration**
   - URL: `http://localhost:8080/api/users/register`
   - Method: POST
   - Purpose: Register new users with their details

2. **Health Check**
   - URL: `http://localhost:8080/api/users/health`
   - Method: GET
   - Purpose: Check if the service is running

3. **User Authentication**
   - URL: `http://localhost:8080/api/users/authenticate`
   - Method: POST
   - Purpose: User login with email and password

### Admin Endpoints

1. **Get All Users**
   - URL: `http://localhost:8080/api/users/all`
   - Method: GET
   - Purpose: View list of all registered users
   - Requires admin authentication

2. **Delete User**
   - URL: `http://localhost:8080/api/users/delete`
   - Method: DELETE
   - Purpose: Remove a user using their email
   - Requires admin authentication

### Admin Credentials
- Username: `admin`
- Password: `admin123`
- Note: Use Basic Authentication in Postman when accessing admin endpoints

## Setup Requirements

- Java 17 or higher
- Maven
- Docker (optional)

## Running the Application
Go to user management task  folder ->
### Local Development

1. Build the application:
 
   mvn clean install
  

2. Run the application:
   
   mvn spring-boot:run
  

### Docker Deployment

1. Build Docker image:
   
   docker build -t user-management-task .


2. Run Docker container:
  
   docker run -p 8080:8080 user-management-task
  

## Testing

- API testing can be done via:
  - Swagger UI (`http://localhost:8080/swagger-ui/index.html`)
  - Postman
- JUnit tests are available for service layer verification
