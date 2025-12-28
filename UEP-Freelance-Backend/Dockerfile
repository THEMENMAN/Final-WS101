# ============================================
# WORKING DOCKERFILE FOR RENDER
# ============================================

# Use working Maven image
FROM maven:3.9.6-eclipse-temurin-17 AS builder
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests

# Use working Java image
FROM eclipse-temurin:17-jre-alpine
WORKDIR /app
COPY --from=builder /app/target/*.jar app.jar

# Render settings
ENV PORT=8080
EXPOSE 8080

# Run Spring Boot
ENTRYPOINT ["java", "-jar", "app.jar"]
