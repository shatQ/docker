# poc-docker

This prove of concept shows how build microservice application based on docker containers that are orchestrated with usage of docker-compose tool.

## Context Path

There are two possibilities to handle context path (e.g. /ui):
- directly in microservice framework (e.g. Boot Spring)
- by reverse proxy (e.g. HAProxy)

Microservice framework ```Spring Boot``` used to build this POC doesn't suppor X-Forwarded-Prefix http header, so it's not possible to change context path by HAProxy. It needs to be done at microservice level by modifying file ```src/main/resources/application.properties``` and appending:

```
server.servlet.context-path: /ui
```
