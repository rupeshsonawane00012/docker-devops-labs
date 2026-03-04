# Docker Commit Lab

1. Run nginx container
docker run -d --name web nginx

2. Enter container
docker exec -it web bash

3. Create HTML file
cd /usr/share/nginx/html
echo "<h1>Hello Docker</h1>" > lab.html

4. Commit container
docker commit web my-nginx:v1

5. Run new container
docker run -d -P my-nginx:v1
