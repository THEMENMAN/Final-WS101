FROM maven:3.8.7-openjdk-17
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests
CMD ["java", "-jar", "target/*.jar"]
