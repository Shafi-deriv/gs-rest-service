
FROM maven:3.8.5-openjdk-17 as build
COPY . .
RUN --mount=type=cache,target=/root/.m2/repository mvn package


FROM openjdk:17.0.2-jdk as runtime
COPY --from=build /target/rest-service-complete-0.0.1-SNAPSHOT.jar .
CMD ["java", "-jar", "rest-service-complete-0.0.1-SNAPSHOT.jar"]




