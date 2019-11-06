FROM maven:3.5-jdk-8 AS build
COPY src /usr/glarimy/src
COPY pom.xml /usr/glarimy
RUN mvn -f /usr/glarimy/pom.xml clean package
EXPOSE 8080
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongodb:27017/glarimy?useSSL=false&allowPublicKeyRetrieval=true","-jar","/usr/glarimy/target/quiz-employee-service-0.0.1-SNAPSHOT.jar"]
