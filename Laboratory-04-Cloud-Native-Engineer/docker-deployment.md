# Docker Deployment

## Docker Environment

### Check Docker Version

docker --version

-This command checks whether Docker is installed and displays the version available in the environment.

### Check Docker Information

docker info

-This command provides details about the Docker server and the current Docker environment.

### Downloading Nginx

Command: docker pull nginx

-This command retrieves the Nginx image from Docker Hub so it can be used to create a container.

### Starting Nginx

Command: docker run -d --name nginx -p 8080:80 nginx

-This command creates an Nginx container, starts it in the background, and connects host port 8080 to port 80 inside the container.

### Checking the Container

Command: docker ps

-This command shows the containers that are currently active.

### Testing the Web Server

Command: curl http://localhost:8080

-This command sends a request to the Nginx service through port 8080 and displays the response returned by the web server.

### Stopping the Container

Command: docker stop nginx

-This command stops the Nginx container without immediately deleting it.

### Checking the Stopped Container

Command: docker ps -a

-This command displays both running and stopped containers so the previous Nginx container can be verified.

### Removing the Container

Command: docker rm nginx

-This command removes the stopped Nginx container from Docker.

### Container Lifecycle

The basic lifecycle demonstrated in this activity was:

Nginx Image
     |
     v
Create and Run
     |
     v
Running Container
     |
     v
Stop
     |
     v
Stopped Container
     |
     v
Remove

### Understanding Port Mapping

The Nginx service listens on port 80 inside the container. The -p 8080:80 option connects port 8080 of the host to port 80 of the container. Because of this connection, the web server can be tested by using localhost:8080.
