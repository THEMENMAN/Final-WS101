FROM openjdk:17-jdk-slim
WORKDIR /app
COPY . .
RUN apt-get update && apt-get install -y maven
RUN mvn clean package -DskipTests    # ← FIXED: "mvn" not "mwn"
CMD ["java", "-jar", "target/*.jar"]
