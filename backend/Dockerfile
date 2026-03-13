# Stage 1: Build the JAR using Maven
FROM maven:3.9.2-eclipse-temurin-17 AS build

WORKDIR /app

# Copy pom and download dependencies
COPY pom.xml .
RUN mvn dependency:go-offline

# Copy source code
COPY src ./src

# Build the jar
RUN mvn clean package -DskipTests

# Stage 2: Run the JAR
FROM eclipse-temurin:17-jdk

WORKDIR /app

# Copy the jar from the build stage
COPY --from=build /app/target/*.jar chattingo-backend.jar

# Expose port
EXPOSE 8080

# Run backend
ENTRYPOINT ["java", "-jar", "chattingo-backend.jar"]