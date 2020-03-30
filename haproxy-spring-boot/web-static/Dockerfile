FROM openjdk:8-jdk-alpine

WORKDIR /app

ARG WAR_FILE

COPY ${WAR_FILE} app.war

EXPOSE 8080

ENTRYPOINT ["java","-jar","/app/app.war"]
