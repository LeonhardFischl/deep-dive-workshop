FROM openjdk as final
WORKDIR /app
EXPOSE 8090
COPY ./btested-0.1.0-SNAPSHOT.jar /app/java-service.jar
CMD ["java", "-jar", "/app/java-service.jar", "hello.Application"]