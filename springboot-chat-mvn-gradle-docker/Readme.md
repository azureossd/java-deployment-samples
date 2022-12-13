
# Springboot Websocket Demo
## Building with Maven

**1. Clone the application**

**2. Build the app using the Maven wrapper**

```bash
cd springboot-chat-mvn-gradle-docker
./mvnw package
```

**3. Run the application**
```bash
java -jar target/websocket-demo-0.0.1-SNAPSHOT.jar
```

Alternatively, you can run the app directly without packaging

```bash
./mvnw spring-boot:run
```
## Building with Gradle


**1. Clone the application**


**2. Build and run the app using Gradle**

```bash
cd spring-boot-websocket-chat-demo
./gradlew assemble
```

**3. Run the application**
```bash
java -jar build/libs/websocket-demo-0.0.1-SNAPSHOT.jar
```
Alternatively, you can run the app directly without packaging

```bash
./gradlew bootRun
```
## Deploying with Docker
**1. Update the Dockerfile with the proper .jar target path for Gradle OR Maven**
```docker
# Application Jar Target path for Maven OR Gradle 

#Maven Path
ARG JAR_FILE=target/websocket-demo-0.0.1-SNAPSHOT.jar

#Gradle Path
ARG JAR_FILE=build/libs/websocket-demo-0.0.1-SNAPSHOT.jar

```
**2. Build the Docker Image**
```docker
Docker build -t springwebsocketdemo:01 .
```
**3. Run the Image**
```
docker run -d -p 8081:8080 springwebsocketdemo:01
```
