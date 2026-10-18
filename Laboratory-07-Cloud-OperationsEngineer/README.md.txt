# Laboratory 07: Cloud Operations Engineer

## 1. Mission Overview

The mission of this laboratory is to simulate the responsibilities of a Cloud Operations Engineer by deploying a web server, generating HTTP traffic, analyzing application logs, and monitoring container resource usage. The lab demonstrates how system baselines and monitoring tools help maintain the availability, performance, and reliability of a web application.

## 2. Objectives

- Check the server's RAM usage and available disk storage.
- Establish a baseline for host system resources.
- Deploy an Nginx web server using Docker.
- Generate HTTP requests to simulate website traffic.
- Produce and investigate an HTTP 404 error.
- Retrieve and analyze application logs using Docker.
- Monitor container CPU, memory, and network usage.
- Document the results, observations, and screenshots.

## 3. Monitoring Commands

### Check Memory Usage

```bash
free -h
```

Displays total, used, free, and available system memory.

### Check Root Filesystem Storage

```bash
df -h /
```

Displays the total, used, and available storage of the root filesystem.

### View Running Processes and CPU Load

```bash
top
```

Displays active processes, CPU utilization, memory usage, and system load averages. Press `q` to exit.

### Deploy the Nginx Container

```bash
docker run -d --name clientwebsite -p 8080:80 nginx
```

Starts an Nginx web server in the background and maps host port 8080 to container port 80.

### Verify the Container

```bash
docker ps
```

Lists currently running Docker containers.

### Generate HTTP Requests

```bash
curl http://localhost:8080
curl http://localhost:8080
curl http://localhost:8080
```

Sends three HTTP requests to the Nginx web server.

### Generate a 404 Error

```bash
curl -i http://localhost:8080/hidden-admin-page
```

Requests a nonexistent page and displays the HTTP response headers and status code.

### Retrieve Application Logs

```bash
docker logs clientwebsite
```

Displays the container's logs, including recorded HTTP requests and error responses.

### Monitor Container Resources

```bash
docker stats
```

Displays live CPU usage, memory consumption, network I/O, block I/O, and process counts for running containers. Press `Ctrl + C` to exit.

## 4. Results and Observations

The laboratory activities demonstrate how to establish a host system baseline, deploy a web server, generate HTTP traffic, and inspect application logs. The `docker stats` command provides real-time resource metrics that help identify potential CPU or memory bottlenecks.

Record the actual RAM, root filesystem storage, CPU usage, memory usage, and HTTP response results observed during the laboratory.

## 5. Screenshots and Evidence

Store the required screenshots in the `screenshots` directory.

- `memory-check.png` — host memory usage.
- `disk-check.png` — root filesystem storage.
- `install-nginx.png` — Nginx container deployment.
- `simulation1.png` — successful HTTP requests.
- `simulation2.png` — HTTP 404 error response.
- `docker-logs.png` — application logs.
- `container-metrics.png` — live Docker resource metrics.

## 6. Conclusion

This laboratory provided practical experience with essential cloud operations tasks, including system resource inspection, Docker container deployment, traffic simulation, application log analysis, and real-time monitoring. These skills help engineers troubleshoot issues, identify resource constraints, and maintain reliable web services.
