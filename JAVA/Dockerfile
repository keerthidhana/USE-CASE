FROM maven:3.9-eclipse-temurin-17 AS builder
WORKDIR /launchpad
COPY java-service/pom.xml .
RUN mvn dependency:go-offline
COPY java-service .
RUN mvn package -DskipTests
 
FROM eclipse-temurin:17-jre
WORKDIR /app
COPY --from=builder /launchpad/target/*.jar app.jar
ENTRYPOINT ["java","-jar","app.jar"]
