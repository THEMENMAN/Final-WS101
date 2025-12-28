FROM eclipse-temurin:17-jdk-alpine
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests
CMD ["java", "-jar", "target/*.jar"]
