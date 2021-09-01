# M21CS015

## Shruti Sureshan (Mtech CSE, Roll no: M21CS015)


### Functionality of the application:
This is a Travel Guide Web Application using Docker, HTML, CSS, JavaScript to help customers book their tours. It connects agents and customers directly. In the traditional system, the customer have to wait in long queues and involves a lot of paperwork. Through this web application, the user can visit the portal, submit their details and then the travel agency can connect with them and book their tours.

### Steps:
1. Create the web application
2. Create the Dockerfile
   - Docker file is used to create the Docker image
   - Docker images is a set of instructions to build a Docker container. The base image should include the platform dependencies required by your application so that your application runs smoothly. So Docker images are built based on contents of Dockerfile. Here the base image is alpine version on nginx webserver.  A base image is an empty first layer which allows to build the Docker images from scratch
3. Build the Dockerfile
```
docker build -t webserver-image:v1 .
```
4. Run the Docker Container
```
docker run -d -p 80:80 webserver-image:v1
```
Output: 4a5fc35e5caa9ad25ceb274da9a839a64e1d48a9f9ba9d5053f3d6c96de21589

The running container can be seen by using the command-
```
docker ps
```
Output:
CONTAINER ID   IMAGE                COMMAND                  CREATED          STATUS          PORTS                               NAMES
4a5fc35e5caa   webserver-image:v1   "/docker-entrypoint.…"   13 seconds ago   Up 12 seconds   0.0.0.0:80->80/tcp, :::80->80/tcp   great_hodgkin

5. Run the application on browser and test the port
```
http://localhost:80
```

6. Push the Docker container image to Docker Hub
   - First create a repository (Repository name: shrutisureshan) and then push the Docker container image using the following command-
```
docker tag webserver-image:v1 shrutisureshan/webserver-image:v1
```

7. Pull the Docker image
   - To pull the Docker image run the following command-
```
docker pull shrutisureshan/webserver-image:v1
```
