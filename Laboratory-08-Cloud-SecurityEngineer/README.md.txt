# Cloud Security Engineer

## Mission Overview

The mission of this laboratory is to deploy a web application using an Nginx Docker container and secure the server using UFW (Uncomplicated Firewall). The configuration demonstrates basic cloud security practices, including restricting incoming traffic, allowing necessary services, and verifying firewall rules.

## Objectives

- Deploy an Nginx web server container named `secure-web-app`.
- Expose the web application through TCP port 8080.
- Test web server connectivity using `curl`.
- Configure UFW to deny incoming traffic by default.
- Allow SSH access for server administration.
- Allow TCP port 8080 for the web application.
- Verify firewall status and document the configuration.

## Commands Executed

### Deploy the Web Application

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
```

### Test Web Application Connectivity

```bash
curl -i http://localhost:8080
```

### Configure the Firewall

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 8080/tcp
sudo ufw enable
```

### Verify Firewall Configuration

```bash
sudo ufw status verbose
sudo ufw status numbered
```

### Check the Docker Container

```bash
docker ps
docker ps -a
docker logs secure-web-app
```

## Skills Learned

- Deploying a web server using Docker.
- Mapping container ports to host ports.
- Testing HTTP connectivity with `curl`.
- Configuring firewall rules with UFW.
- Applying the Principle of Least Privilege and the Default Deny policy.
- Allowing specific ports while restricting unnecessary incoming traffic.
- Understanding the importance of permitting SSH before enabling a firewall.
- Documenting technical procedures and security configurations using Markdown.
