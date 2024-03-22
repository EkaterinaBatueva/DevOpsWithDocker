FROM amazoncorretto:8

WORKDIR /usr/src

EXPOSE 8080

# Copy all of the source code
COPY . .

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]