# Start with a base image containing Java runtime (adoptopenjdk is open source and good for production)
FROM adoptopenjdk:11-jre-hotspot

# Add Maintainer Info
LABEL maintainer="nasa.kino7@gmail.com"

# Add a volume pointing to /tmp
VOLUME /tmp

# Make port 8080 available to the world outside this container
EXPOSE 8080

# The application's jar file (when packaged)
ARG JAR_FILE=target/SpringBootHelloWorldExampleApplication-1.jar

# Add the application's jar to the container
ADD ${JAR_FILE} my-spring-boot-app.jar

# Run the jar file
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/my-spring-boot-app.jar"]
