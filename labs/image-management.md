# 🐳 Docker Image Management Lab

This lab demonstrates how to manage Docker images including pulling, listing, removing, tagging, and cleaning unused images.

---

# Objective

Learn how to:

- Pull images from Docker Hub
- View available images
- Remove images
- Tag images
- Clean unused images

---

# Step 1: Pull an Image

Download an image from Docker Hub.

```bash
docker pull nginx

Explanation:

Command	Meaning
docker pull	Downloads image from registry
nginx	Image name

Verify the image:

docker images

Example output:

REPOSITORY   TAG       IMAGE ID       SIZE
nginx        latest    xxxxxxxxx      240MB
Step 2: List Docker Images

Display all locally stored Docker images.

docker images

This shows:

Repository name

Tag

Image ID

Size

Creation time

Step 3: Remove an Image

Remove an image using its name.

docker rmi nginx

Or using image ID:

docker rmi <image_id>

Example:

docker rmi 0236ee02dcbc
Step 4: Tag an Image

Tagging assigns a new name to an image.

docker tag nginx my-nginx:v1

Check images:

docker images

Example:

REPOSITORY   TAG   IMAGE ID
nginx        latest
my-nginx     v1
Step 5: Remove Unused Images

Remove dangling images:

docker image prune

Remove all unused images:

docker image prune -a

Docker will ask confirmation:

Are you sure you want to continue? [y/N]

Type:

y
Docker Image Naming Convention

Docker images follow this format:

registry/namespace/repository:tag

Examples:

nginx
nginx:1.25
username/myapp:1.0

If no tag is specified, Docker uses:

latest
Docker Image Workflow
Pull → Store → Run → Remove

Example workflow:

docker pull nginx
docker images
docker run nginx
docker rmi nginx
Key Takeaways

Docker images are read-only templates used to create containers.

Images can be pulled from registries like Docker Hub.

Images can be tagged and reused.

Unused images should be cleaned to save disk space.

Author
Rupesh Gorakhnath Sonawane
DevOps & Cloud Enthusiast
