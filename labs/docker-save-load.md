# 🐳 Docker Save and Load Lab

This lab demonstrates how to export and import Docker images using the  
`docker save` and `docker load` commands.

These commands are useful when transferring images between systems or
working in offline environments.

---

# Objective

Learn how to:

- Save a Docker image to a `.tar` file
- Transfer Docker images between systems
- Load an image back into Docker

---

# Step 1: Pull an Image

Pull the nginx image from Docker Hub.

```bash
docker pull nginx

Verify the image:

docker images

Example output:

REPOSITORY   TAG       IMAGE ID
nginx        latest    xxxxxxxxx
Step 2: Save the Image to a TAR File

Use the docker save command to export the image.

docker save -o nginx-image.tar nginx

Explanation:

Part	Meaning
docker save	Export image
-o	Output file
nginx-image.tar	File name
nginx	Image name

Check the file:

ls

You should see:

nginx-image.tar
Step 3: Remove the Image (Optional Test)

Remove the image to simulate transferring it to another system.

docker rmi nginx

Verify removal:

docker images
Step 4: Load the Image Back

Import the image using docker load.

docker load -i nginx-image.tar

Verify the image is restored:

docker images

Example output:

REPOSITORY   TAG       IMAGE ID
nginx        latest    xxxxxxxxx
Step 5: Run Container from Loaded Image

Run a container to confirm the image works.

docker run -d -p 8080:80 nginx

Open in browser:

http://localhost:8080

You should see the NGINX welcome page.

Docker Save vs Export
Command	Purpose
docker save	Saves Docker image
docker export	Saves container filesystem

Example:

docker export container_id > container.tar
Use Cases

Moving images between servers

Offline installations

Backup of Docker images

CI/CD pipeline artifact storage

Key Takeaways

docker save exports images to a .tar archive.

docker load imports images from a .tar archive.

Useful for transferring images without a registry.

Author:
Rupesh Gorakhnath Sonawane
DevOps & Cloud Enthusiast
