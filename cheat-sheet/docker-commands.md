# Docker Commands Cheat Sheet

## Images
docker pull nginx
docker images
docker rmi nginx

## Containers
docker run nginx
docker run -d nginx
docker run -d -p 8080:80 nginx

docker ps
docker ps -a

docker stop container
docker start container
docker rm container

## Interaction
docker exec -it container bash
docker logs container
docker inspect container

## Image Operations
docker commit container image:v1
docker save -o image.tar image:v1
docker load -i image.tar

## Cleanup
docker image prune
docker system prune -a
