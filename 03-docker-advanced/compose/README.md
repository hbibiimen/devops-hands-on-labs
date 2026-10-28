# Docker Compose - Nginx Hands-on Lab

## Objective
Deploy an Nginx web server using Docker Compose.

## Technologies
- Docker
- Docker Compose v5.6.1
- Nginx Alpine

## Configuration
- Service: web
- Image: nginx:alpine
- Host port: 8091
- Container port: 80
- Network: compose_default

## Test result
HTTP/1.1 200 OK - Nginx web server successfully deployed.

## Commands used

```bash
sudo docker compose up -d
sudo docker compose ps
sudo docker compose config
curl -I http://localhost:8091
sudo docker compose down
```

Run Docker Compose commands from the directory containing compose.yaml.
