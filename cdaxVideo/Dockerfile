# Use official Java 17 base image
FROM eclipse-temurin:17-jdk-jammy

# Set working directory
WORKDIR /app

# Copy project files
COPY . .

# Build jar
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# Expose port
EXPOSE 8080

# Run Spring Boot jar
CMD ["java", "-jar", "target/cdaxVideo-0.0.1-SNAPSHOT.jar"]
