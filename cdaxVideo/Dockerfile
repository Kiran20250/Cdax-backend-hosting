# Use official OpenJDK 17 image
FROM openjdk:17-jdk-slim

# Set working directory inside container
WORKDIR /app

# Copy Maven wrapper + pom.xml and source code
COPY . .

# Build the project
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# Expose port (Render auto assigns PORT, but default is 8080)
EXPOSE 8080

# Run Spring Boot JAR file
CMD ["java", "-jar", "target/cdaxVideo-0.0.1-SNAPSHOT.jar"]
