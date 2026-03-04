# 🐳 Docker Commit Lab

This lab demonstrates how to create a new Docker image from a running container using the `docker commit` command.

---

# Objective

Learn how to:

- Run a container
- Modify the container
- Create a new image from the container
- Run a container from the new image

---

# Step 1: Pull NGINX Image

Pull the image from Docker Hub.

```bash
docker pull nginx

Verify image:

docker images
Step 2: Run a Container

Run a container from the nginx image.

docker run -d --name web nginx

Check running containers:

docker ps
Step 3: Access the Container

Enter the running container.

docker exec -it web bash
Step 4: Modify the Container

Go to the NGINX web directory.

cd /usr/share/nginx/html

Create a new HTML file.

echo "<h1>Hello from Docker Commit Lab</h1>" > lab.html

Verify file:

ls

Exit container:

exit
Step 5: Commit the Container

Create a new image from the modified container.

docker commit web my-nginx:v1

Check images:

docker images

Example output:

REPOSITORY   TAG   IMAGE ID
my-nginx     v1    xxxxxxxxx
Step 6: Run Container from New Image

Run a new container from the committed image.

docker run -d -P --name test my-nginx:v1

Check container:

docker ps

Example port mapping:

0.0.0.0:32769 -> 80/tcp
Step 7: Access in Browser

Open:

http://<server-ip>:32769/lab.html

You should see:

Hello from Docker Commit Lab
Docker Workflow
Image → Container → Modify → Commit → New Image → New Container
Key Takeaways

docker commit creates a new image from a container.

Useful for quick testing and debugging.

In production environments, Dockerfiles are preferred for building images.

Author: Rupesh Gorakhnath Sonawane
DevOps & Cloud Enthusiast
