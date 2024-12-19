From ubuntu:latest AS jay
WORKDIR /app
COPY . .
RUN apt-get update && apt-get upgrade -y
RUN apt-get install openjdk-11-jre -y && apt-get install maven -y
RUN mvn clean package
WORKDIR target
CMD ["java","-jar","spring-boot-web.jar"]
