Docker Steps
Building maven build
build jar file using the command :mvn clean package: at the project directory in cmd. Create a docker file with no extension. write the following in Dockerfile FROM openjdk:8-jdk-alpine VOLUME /tmp ADD demo-0.0.1-SNAPSHOT.jar ./ ADD dailyweather.csv ./ ENTRYPOINT ["java","-jar","demo-0.0.1-SNAPSHOT.jar"]

This will add all dependencies in docker file

Moving resources to ec2
transfer jar file to ec2

commands in ec2 to run build jar file
sudo docker build . sudo docker run -p 8080:8080 (image id)

pushing Image
sudo docker tag tagid username/repositoryname:image name sudo docker push username/repositoryname sudo docker run -p 8080:8080 has1th/myfirstboot:yoyo
