FROM openjdk:17-jdk-alpine

COPY *.jar app.jar
expose 8080
ENTRYPOINT ["java","-jar","/app.jar"]