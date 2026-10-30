# Docker Swarm - Nginx Hands-on Lab

## Objective
Deploy and manage an Nginx web service using Docker Swarm.

## Environment
- Ubuntu 22.04
- Docker Engine 29.1.3
- Docker Swarm single-node cluster
- Manager node: serveur (192.168.56.10)

## Technologies
- Docker
- Docker Swarm
- Nginx Alpine
- Linux CLI

## Practical Exercises

### 1. Initialize Docker Swarm

```bash
sudo docker swarm init --advertise-addr 192.168.56.10
sudo docker node ls
```

Result: Manager node Ready, Active and Leader.

### 2. Deploy Nginx with two replicas

```bash
sudo docker service create --name nginx-swarm --replicas 2 --publish 8092:80 nginx:alpine
sudo docker service ls
sudo docker service ps nginx-swarm
```

Result: 2/2 replicas running.

### 3. Horizontal Scaling

```bash
sudo docker service scale nginx-swarm=3
sudo docker service ps nginx-swarm
```

Result: 3/3 replicas running.

### 4. HTTP Connectivity Test

```bash
curl -I http://localhost:8092
```

Result: HTTP/1.1 200 OK.

### 5. Self-Healing Test

```bash
sudo docker ps --filter label=com.docker.swarm.service.name=nginx-swarm
sudo docker stop <container_id>
sudo docker service ps nginx-swarm
```

Result: Docker Swarm automatically replaced the stopped container and restored three running replicas.

### 6. Scale Down

```bash
sudo docker service scale nginx-swarm=1
sudo docker service ls
```

Result: 1/1 replica running.

### 7. Clean Up

```bash
sudo docker service rm nginx-swarm
```

Result: Nginx service removed successfully.

## Skills Demonstrated
- Container orchestration
- Docker Swarm cluster initialization
- Service deployment and management
- Horizontal scaling
- Self-healing
- HTTP connectivity testing
- Service lifecycle management

## Conclusion
Successfully deployed and managed an Nginx service using Docker Swarm on a single-node cluster. Validated horizontal scaling, automatic task replacement and HTTP connectivity.
