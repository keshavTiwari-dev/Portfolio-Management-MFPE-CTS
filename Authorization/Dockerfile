FROM openjdk:8
ADD target/Authorization-docker.jar Authorization-docker.jar
EXPOSE 8081
ENTRYPOINT ["java","-jar","Authorization-docker.jar"]