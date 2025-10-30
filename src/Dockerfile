# Use OpenJDK 17 as the base image
FROM openjdk:17-jdk-slim

# Set working directory inside container
WORKDIR /app

# Copy Gradle wrapper and build files
COPY build.gradle .
COPY settings.gradle .
COPY gradlew .
COPY gradlew.bat .
COPY gradle ./gradle

# Copy the rest of the source code
COPY . .

# Build the application
RUN ./gradlew build -x test

# Expose port 8080 for Cloud Run
EXPOSE 8080

# Run the JAR file
CMD ["java", "-jar", "build/libs/*.jar"]
