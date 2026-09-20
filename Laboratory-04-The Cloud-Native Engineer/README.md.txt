### Mission Overview

This laboratory activity focused on understanding cloud-native technologies, particularly Docker containers. The mission involved comparing traditional Virtual Machines (VMs) with containers, entering a Docker-enabled cloud environment, deploying an Nginx web server, and managing the container lifecycle. The activities also provided hands-on experience with Docker commands and technical documentation using Markdown.

## Objectives

* Differentiate between Virtual Machines (VMs) and containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI commands.
* Pull and run a containerized Nginx web server.
* Map a host port to a container port.
* Manage the lifecycle of a Docker container.
* Document container operations using Markdown.
* Maintain and organize the Cloud Computing GitHub portfolio.

## Docker Commands Executed

### Checkpoint 3 - Docker Playground

docker --version
docker info

* `docker --version` — Displays the installed Docker version.
* `docker info` — Displays information about the Docker environment.

### Checkpoint 4 - Deploy Nginx

docker pull nginx
docker run -d -p 8080:80 --name nginx-server nginx
curl http://localhost:8080

* `docker pull nginx` — Downloads the official Nginx image.
* `docker run -d -p 8080:80 --name nginx-server nginx` — Creates and runs the Nginx container in detached mode and maps host port 8080 to container port 80.
* `curl http://localhost:8080` — Sends an HTTP request to verify that the Nginx web server is running.

### Checkpoint 5 - Container Lifecycle

docker ps
docker stop nginx-server
docker ps
docker ps -a
docker rm nginx-server

* `docker ps` — Lists currently running containers.
* `docker stop nginx-server` — Stops the Nginx container.
* `docker ps` — Verifies that the Nginx container is no longer running.
* `docker ps -a` — Lists all containers, including stopped containers.
* `docker rm nginx-server` — Removes the stopped Nginx container.

## Skills Learned

Through this laboratory activity, I learned how to work with Docker in a cloud-based Linux environment. I learned how to check the Docker installation, download images, create and run containers, map network ports, and verify a web server using `curl`. I also learned how to stop, inspect, and remove containers and how to document technical procedures using Markdown and GitHub.

## Challenges Encountered

One challenge was becoming familiar with Docker commands and understanding the difference between a Docker image and a running container. Another challenge was understanding how port mapping works when connecting the host port `8080` to the container port `80`. Managing the container lifecycle also required careful execution of the commands in the correct order. Overall, the activity helped me become more comfortable with Docker and cloud-native container management.
