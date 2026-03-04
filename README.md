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

## Example Workflow

```
docker pull nginx
docker create nginx
docker start <container_id>
docker exec -it <container_id> bash
cd /usr/share/nginx/html
echo "<h1>Hello Docker Lab</h1>" > lab.html
docker commit <container_id> my-nginx:v1
docker run -d -P my-nginx:v1
```

## Docker Lifecycle

Image → Container → Modify → Commit → New Image

---

Author: Rupesh  Sonawane
DevOps & Cloud Enthusiast
