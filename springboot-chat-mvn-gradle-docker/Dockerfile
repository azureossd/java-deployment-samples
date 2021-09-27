# Java runtime base image
FROM openjdk:8-jdk-alpine

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Application Jar Target path for Maven or Gradle 
#ARG JAR_FILE=target/websocket-demo-0.0.1-SNAPSHOT.jar
ARG JAR_FILE=build/libs/websocket-demo-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} websocket-demo.jar

# Run the jar file 
ENTRYPOINT ["java","-jar","/websocket-demo.jar"]