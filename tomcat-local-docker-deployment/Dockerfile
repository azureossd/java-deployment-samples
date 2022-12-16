# Pull an image using Tomcat 9.0.70, with a Eclipse Temurin JDK 17 version
# Using jammy (Ubuntu's codename for Ubuntu 22)
FROM tomcat:9.0.70-jdk17-temurin-jammy

ARG WAR_FILE=ROOT.war
# Delete the existing ROOT directory
RUN rm -rf /usr/local/tomcat/webapps/ROOT
# Copy our ROOT.war into this location since this is where Tomcat runs applications from by default
COPY ${APP_FILE} /usr/local/tomcat/webapps/

EXPOSE 8080

CMD ["catalina.sh", "run"]