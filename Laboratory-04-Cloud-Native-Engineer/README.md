# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

This laboratory focused on containerization and the basic use of Docker. I worked with the KillerCoda environment to check the Docker installation, obtain an Nginx image, create a web server container, and manage that container from start to finish.

## Objectives

- Explain the main differences between virtual machines and containers.
- Work with Docker through the KillerCoda environment.
- Practice common Docker commands.
- Deploy an Nginx web server inside a container.
- Test a containerized web service using a local port.
- Practice stopping and removing containers.
- Organize the laboratory work in a GitHub portfolio.

## Docker Commands Executed

### Check Docker Version

docker --version

### Check Docker Environment

docker info

### Download Nginx

docker pull nginx

### Create and Start the Container

docker run -d --name nginx -p 8080:80 nginx

### Check Running Containers

docker ps

### Test Nginx

curl http://localhost:8080

### Stop the Container

docker stop nginx

### Display All Containers

docker ps -a

### Delete the Container

docker rm nginx

### Skills Learned

This activity gave me practical experience with Docker instead of only reading about containers. I learned how an image can be downloaded and used to create a running application environment. I also practiced checking containers, connecting a host port to a container port, and cleaning up a container after testing.

### Challenges Encountered

The main challenge was remembering the purpose of the different Docker commands and understanding the relationship between an image and a container. Port mapping was also something I had to understand because the Nginx service uses port 80 inside the container while I accessed it through port 8080 on the host.
