#Use Java as a base image
FROM eclipse-temurin:17-jdk-alpine

#Define place to put the application in the container
WORKDIR /app

#Set port for application to use
EXPOSE 8080

#Add the jar file
ADD /target/*.jar viabackend-0.0.1-SNAPSHOT.jar

#Start the application
ENTRYPOINT [ "java", "-jar", "/app/viabackend-0.0.1-SNAPSHOT.jar" ]
