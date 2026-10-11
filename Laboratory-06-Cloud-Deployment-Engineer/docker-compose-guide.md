# Docker Compose Guide

## 1. What Does the `services:` Block Do?

The `services:` block defines the containers that make up the application. In our Docker Compose file, there are two services: `database` and `app`. The `database` service uses the `mariadb:10.6` image to store data, while the `app` service uses the `nextcloud` image to provide the web interface. Docker Compose manages both services and creates a network that allows them to communicate.

## 2. How Does Nextcloud Find the Database Container?

The Nextcloud application finds the database container through the `MYSQL_HOST` environment variable, which is set to `database`. This value matches the service name defined under the `services:` block in the Docker Compose file. Docker Compose provides internal DNS resolution, allowing the Nextcloud container to locate and communicate with the MariaDB container using the service name `database`.

## 3. Difference Between `docker run` and `docker-compose up -d`

The `docker run` command starts an individual container and requires us to specify its configuration through command-line options. When deploying multiple containers, we may need to configure their networks and environment variables separately.

The `docker-compose up -d` command reads the `docker-compose.yml` file and creates or starts all the services defined in it. The `-d` option runs the containers in detached mode, allowing them to run in the background while the terminal remains available. Docker Compose simplifies multi-container deployment by managing services, networks, and configurations in one file.

## Conclusion

Docker Compose makes deploying multi-container applications easier by defining the application's infrastructure in a single YAML file. In this project, Nextcloud and MariaDB run in separate containers and communicate through the Docker Compose network.
