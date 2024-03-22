FROM maven:3.8-jdk-8  

COPY . . 

RUN mvn package

CMD ["java" ,"-jar" ,"./target/docker-example-1.1.3.jar"]  

EXPOSE 8080
