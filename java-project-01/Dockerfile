# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM openjdk:11

# Copy the source code to the container
COPY . .

#Install maven and build the application
RUN apt-get update && \
    apt-get install -y maven && \
    mvn package -DskipTest

#Expose port 
EXPOSE 8080

# This should not be changed
ENTRYPOINT ["java","-jar","target/spring-boot-web.jar"]
