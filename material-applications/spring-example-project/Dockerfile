# Choose Amazon Corretto 8 as the base image for Java 8 support
FROM amazoncorretto:8

WORKDIR /app

# Copy the build jar file into the container
COPY target/docker-example-1.1.3.jar app.jar

# Expose port 8080 for the application
EXPOSE 8080

# Run the jar file
ENTRYPOINT ["java","-jar","app.jar"]

