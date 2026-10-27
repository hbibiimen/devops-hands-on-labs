# Docker Fundamentals - Hands-on Lab

## Project Overview
This hands-on lab demonstrates practical Docker skills: managing images and containers, deploying Nginx, building custom images with Dockerfile, using Docker volumes and bind mounts, and working with Docker registries.

## Build the Docker Image

```bash
docker build -t mon-site-devops:v1 .
```

## Run the Container

```bash
docker run -d --name devops-demo -p 8091:80 mon-site-devops:v1
```

Access the website at http://localhost:8091
