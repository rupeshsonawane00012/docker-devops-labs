# 🐳 Docker DevOps Practice Labs

This repository contains hands-on labs and practice exercises for learning Docker as part of my DevOps journey.

## Topics Covered

- Docker container lifecycle
- Image management
- Running containers
- Port mapping
- Environment variables
- Docker exec and file copy
- Inspecting and monitoring containers
- Creating images using docker commit
- Saving and loading images
- Docker Hub workflow

---

## 🧪 Labs Included

### Container Management
- docker create
- docker run
- docker start
- docker stop
- docker rm
- docker ps

### Exposing Applications
- docker run -p
- docker run -P
- environment variables

### Container Interaction
- docker exec
- docker cp

### Troubleshooting
- docker inspect
- docker logs
- docker stats

### Image Management
- docker pull
- docker images
- docker rmi
- docker commit
- docker save
- docker load
- docker image prune

---

## Example Lab Workflow

```bash
docker pull nginx
docker create nginx
docker start <container_id>
docker exec -it <container_id> bash
cd /usr/share/nginx/html
echo "<h1>Hello Docker Lab</h1>" > lab.html
docker commit <container_id> my-nginx:v1
docker run -d -P my-nginx:v1
```
Docker Lifecycle
Image → Container → Modify → Commit → New Image

Tools Used
Docker
Linux
AWS EC2
Docker Hub

Author
Rupesh  Sonawane
DevOps & Cloud Enthusiast
