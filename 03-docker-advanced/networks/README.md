# Docker Networking - Hands-on Lab

## Objective
Create a custom Docker bridge network and verify communication between two Alpine Linux containers.

## Network configuration
- Network: reseau-devops
- Driver: bridge
- Subnet: 172.18.0.0/16
- Gateway: 172.18.0.1
- container1: 172.18.0.2
- container2: 172.18.0.3

## Test result
Communication verified using ping: 4 packets sent, 4 received, 0% packet loss.

## Commands used

```bash
docker network create reseau-devops
docker network ls
docker run -itd --name container1 --network reseau-devops alpine
docker run -itd --name container2 --network reseau-devops alpine
docker exec container1 ping -c 4 container2
docker network inspect reseau-devops
```
