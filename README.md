User Management System
=========================
This is a Spring Boot-based User Management System that allows users to register, authenticate, and provides admin functionalities.
It includes security features like Basic Authentication, IP tracking, Swagger documentation.

Features:
============
Users can register with their name, email, gender, and password.
Email addresses must be unique to prevent duplicate registrations.
The system tracks the user's IP address and country.
Users can authenticate using their email and password.
Basic Authentication is implemented for security.
Admin users have the ability to view all registered users and delete a user by email.
JUnit test cases are included for the service layer.
API documentation and testing are available through Swagger.Url=http://localhost: 8080/swagger-ui/index.html
The application can be containerized using Docker.
API Endpoints:
User Registration: Users can register with their details. url http://localhost:8080/api/users/register
Health Check: A simple endpoint to check if the service is running. url=http://localhost: 8080/api/users/health
User Authentication: Users can log in using their email and password. url-http://localhost: 8080/api/users/authenticate
Get All Users (Admin Only): Admins can view a list of all registered users.
ur1-http://localhost:8080/api/users/all
Delete User (Admin Only): Admins can remove a user from the system using their email. url= http://localhost: 8080/api/users/delete
For admin endpoints, use the following credentials:
Username: admin
Password: admin123
In Postman, select "Basic Auth" and enter the credentials when making requests.

Running the Application:
============================
You need Java 17+, Maven, and Docker installed.
To build and run the application locally, use Maven.
The application can also be run inside a Docker container.
Testing:
The APIs can be tested using Postman or Swagger UI.
JUnit test cases can be executed to verify the service layer functionality.

=============================================================

Deployment:
Build the application using Maven.
Create a Docker image and run it.
build and run locally
mvn clean install mvn 
spring-boot: run
###
Build and Run with Docker
docker build -t user-management-task .
docker run -p 8080:8080 user-management-task
