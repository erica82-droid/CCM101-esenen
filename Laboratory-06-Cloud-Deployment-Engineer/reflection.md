# Mission Reflection

This laboratory activity helped me understand how Docker Compose simplifies the deployment of cloud applications and how different components work together to create a functional system.

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because it allows multiple containers, their configurations, environment variables, and network settings to be defined in one file. Instead of manually typing several Docker commands, an engineer can use a single command, such as `docker-compose up -d`, to deploy the entire application. This approach saves time, reduces repetitive work, and makes deployments easier to reproduce and maintain.

YAML indentation is very important because it determines the structure and relationships between configuration elements. If I make an indentation error or use a Tab instead of spaces, Docker Compose may fail to read the file and display an error. This taught me to be careful when writing configuration files and to check the formatting before deploying an application.

We used environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` to configure the connection between Nextcloud and MariaDB. These variables allow the containers to use consistent database settings without hardcoding the configuration directly into the application. However, sensitive values should be protected using appropriate secrets management practices, especially in production environments.

Deploying Nextcloud in just a few minutes was an exciting and rewarding experience. I was able to see how a cloud storage application and its database could run in separate containers and communicate with each other. It made cloud computing feel more practical and understandable because I could perform the deployment myself rather than simply reading about it.

Since Mission 1, my understanding of cloud computing has evolved from learning basic concepts to understanding how applications can be deployed and managed using containerization. I learned that cloud engineering involves more than running an application; it also requires proper architecture, networking, configuration, security, and documentation. Overall, this activity improved my confidence in using Docker and helped me appreciate how automation makes cloud infrastructure more efficient, reliable, and manageable.
