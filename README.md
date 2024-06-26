### Docker
Its a Containerization platform to run application in container within minimum dependency.

### Virtual Machines (VMs):
1. VM is a complete operating system.
2. It takes more disk space compared to containers and Its heavy
3.  Its less portable

### Containers:
1. It package applications in containers, allowing them to be portable to any operating system
2. It takes minimum dependency to run application and Its lightweight 
3. Portable

### Disadvantages of Container 
1. Container is ephemeral(short life) in nature
2. Doesn’t support Auto healing 
3. Doesn’t support Auto Scaling 
4. Single host support
5. Doesn’t support Enterprise grade service

### Docker Architecture
![docker-architecture](https://user-images.githubusercontent.com/43399466/217507877-212d3a60-143a-4a1d-ab79-4bb615cb4622.png)

### Entrypoint and Cmd:
`ENTRYPOINT` sets the main executable for the container, and `CMD` provides default arguments for that executable or specifies the command to run if `ENTRYPOINT` is not used.

### Most used Docker Commands
1. To build image:
* `docker build -t my_image:latest .`
2. To run image:
* `docker run -d --name my_container nginx`
3. To show running container:
* `docker ps`
4. To push image:
* `docker push myusername/my_image:latest`
5. To pull image:
* `docker pull ubuntu:latest`
6. To stop container:
* `docker stop my_container`
7. To remove container:
* `docker rm my_container`

### Multi stage Build
Create docker images using multiple stages within a single Dockerfile and the final image is so smaller

### Distroless Images
Its a very minimalistic and lightweight docker images that'll only have runtime environment 

### Base images vs Distroless Images
- Base images in Docker contain a minimal operating system with essential components.
- Distroless images is more minimalistic by excluding unnecessary tools and libraries, focusing solely on the application and its dependencies.

### Docker Volume 
Docker volumes are managed by Docker and stored outside the container filesystem.
### Bind Mount
Bind mounts link a directory on the host machine directly to a directory in the container.
### Docker Networking
#### Bridge Network:
it enable containers on the same Docker host to communicate with each other using default virtual eath0
#### Host Network:
Docker container shares its own network with the host machine. The container have no ip address so that it can directly access from host ip.
### Docker compose:
It allows to define and manage multi-container applications in a single YAML file
