# Java runtime base image
FROM openjdk:11-jdk

WORKDIR /app

# Application Jar Target path for Maven or Gradle 
ARG JAR_FILE=target/websocket-demo-0.0.1-SNAPSHOT.jar
# ARG JAR_FILE=build/libs/websocket-demo-0.0.1-SNAPSHOT.jar

# Copy the application's jar to the container
COPY ${JAR_FILE} websocket-demo.jar

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Run the jar file 
ENTRYPOINT ["java","-jar","/app/websocket-demo.jar"]