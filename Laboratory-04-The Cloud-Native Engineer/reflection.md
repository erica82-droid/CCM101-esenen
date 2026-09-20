# Mission Reflection

In this laboratory activity, I learned how Docker containers are different from Virtual Machines and how containers can make application deployment faster and more efficient. One of the biggest differences I noticed is the boot time. A Virtual Machine needs to start a complete operating system, which can take several minutes. In comparison, a Docker container can start in seconds because it shares the host operating system. This makes containers useful when applications need to be deployed quickly.

The port mapping `-p 8080:80` is necessary because the Nginx web server is running inside the container on port 80, while I need to access it through port 8080 on the host machine. The mapping connects the host port 8080 to the container's port 80. By using `curl http://localhost:8080`, I was able to verify that the Nginx web server was running successfully.

I also learned that using `docker rm` removes the container from Docker after it has been stopped. This means that the container itself and its writable data are removed. Because of this, important data should not be stored only inside a container if it needs to remain after the container is removed.

Containerization can also improve the way developers and IT operations teams work together. Developers can package applications with their required environment, while operations teams can deploy those containers consistently. This can make deployment and collaboration easier in a DevOps environment.

Finally, my GitHub portfolio is slowly becoming more organized and complete. Adding this laboratory shows my progress in learning cloud computing, Docker, containers, and technical documentation. I can also use this portfolio to show the skills and activities I have completed throughout the course.

