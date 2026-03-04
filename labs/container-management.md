# 🐳 Docker Container Management Lab

This lab demonstrates how to create, run, manage, and remove Docker containers.

---

# 1. Create a Container

Creates a container from an image but does not start it.

```bash
docker create --name my_container ubuntu

Check containers:

docker ps -a
2. Run a Container

Runs a container interactively.

docker run -it ubuntu

Explanation:

-i → Interactive mode

-t → Terminal access

Exit container:

exit
3. Run Container in Background

Runs container in detached mode.

docker run -d --name web nginx

Check running containers:

docker ps
4. Stop a Container

Stops a running container.

docker stop web
5. Start a Container

Starts a stopped container.

docker start web
6. Remove a Container

Removes a stopped container.

docker rm web
7. List Running Containers

Displays active containers.

docker ps

Example Output:

CONTAINER ID   IMAGE   STATUS   PORTS
8. List All Containers

Displays running and stopped containers.

docker ps -a
Docker Container Lifecycle
Create → Start → Run → Stop → Remove

Example Workflow:

docker pull nginx
docker create nginx
docker start <container_id>
docker stop <container_id>
docker rm <container_id>
Key Takeaways

Containers are instances of Docker images.

Containers can be started, stopped, and removed anytime.

docker ps helps monitor running containers.

docker ps -a shows all containers.

Author: Rupesh Gorakhnath Sonawane
DevOps & Cloud Enthusiast


---

If you want, I can also give you the **next files for your repo**:

- `image-management.md`
- `docker-commit-lab.md`
- `docker-save-load.md`
- `docker-hub-workflow.md`

So your **GitHub repo will look like a real DevOps learning project**. 🚀
