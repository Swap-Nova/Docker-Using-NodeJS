## Why Docker?
Docker will create containerized applications that run on any type of environment that have all the dependencies within it.

```Fundamentals of Docker```
1. Docker Engine
2. Docker Container
3. Docker Image

### What is Docker Engine?
The Docker engine is an open-source containerization technology you can use to build a containerizing application. To simplify, the software that hosts the containers is called Docker Engine.

### What is a Docker Container?
A container is a standard unit of software that packages up the code and all required dependencies needed to run an application on different platforms or computing environments.

### What is a Docker Image?
A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application. It includes code, runtime, system tools, system libraries, and settings.

<hr>

## Docker Hub
Docker Hub is the largest community for Docker images. It allows you to share the container images among your team, or the Docker community. Docker Hub is sort of like GitHub. Here, Docker images reside instead of the project's code.

```Dockerfile commands to build NodeJS project```
```docker
FROM node:latest
WORKDIR /app
COPY . /app
RUN npm install
EXPOSE 8000
CMD ["npm","start"]
```

## Building Docker Image
```bash
docker build -t image_name:version_number .
```
<img width="531" alt="Screenshot 2023-03-22 at 1 52 50 PM" src="https://user-images.githubusercontent.com/92979885/226850606-2d63ce78-f998-4905-8a7d-4b60b173e1c1.png">


Sample Output

## Run Docker Image
```bash
docker container run -d --name <name_of_app> -p <local_port>:<docker_port> <image_name>:<version>
```
<img width="1242" alt="Screenshot 2023-03-22 at 1 55 42 PM" src="https://user-images.githubusercontent.com/92979885/226850978-33f0d5d5-e1df-4ab5-a8dc-cc3538e71a08.png">


## Docker Hub
- `docker login`

After a successful login, you can push the image to Docker hub:

- `docker push <docker_image>:<image_version>`
<img width="886" alt="Screenshot 2023-03-22 at 2 04 49 PM" src="https://user-images.githubusercontent.com/92979885/226851081-c18d7194-9bc2-40c0-a831-4b8e4a33c516.png">

## Output 
<img width="582" alt="Untitled" src="https://user-images.githubusercontent.com/92979885/226851237-61689d1f-fe48-4f3c-a4a5-181b5e5d675e.png">

