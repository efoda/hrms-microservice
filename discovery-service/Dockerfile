FROM maven As first
RUN mvn clean package

FROM openjdk:8-jdk-alpine
ADD target/discovery-service.jar discovery-service.jar
EXPOSE 8761
ENTRYPOINT ["java", "-jar", "/discovery-service.jar"]
