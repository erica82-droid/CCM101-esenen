# Docker Container Lifecycle

## 1. List Running Containers

docker ps


This command lists all currently running Docker containers, including the Nginx container.

## 2. Stop the Container

docker stop nginx-server

This command stops the running Nginx container without removing it.

## 3. Verify the Container Is Stopped

docker ps

This command verifies that the Nginx container is no longer running.

docker ps -a

This command displays all containers, including stopped containers, allowing us to confirm that `nginx-server` still exists.

## 4. Remove the Container

docker rm nginx-server

This command permanently removes the stopped Nginx container.

## Result

The Nginx container was successfully listed, stopped, verified as stopped, and removed from the Docker environment.

