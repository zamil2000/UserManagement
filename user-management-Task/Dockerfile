FROM openjdk:17-jdk

WORKDIR /app

#COPY target/*.jar /app/user-management-task.jar
COPY target/user-management-task.jar app.jar


EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
