# [English] Bash docker usage: Manage containerized applications

## Overview
The `docker` command is a powerful tool used to manage containers, which are lightweight, portable, and self-sufficient units that can run software in a consistent environment. Docker enables developers to package applications and their dependencies into containers, ensuring that they work seamlessly across different computing environments.

## Usage
The basic syntax of the `docker` command is as follows:

```bash
docker [options] [arguments]
```

## Common Options
- `run`: Create and start a container from an image.
- `ps`: List running containers.
- `stop`: Stop a running container.
- `rm`: Remove one or more containers.
- `images`: List all images on the local machine.
- `pull`: Download an image from a Docker registry.
- `build`: Build an image from a Dockerfile.

## Common Examples
Here are some practical examples of using the `docker` command:

1. **Run a Container**
   ```bash
   docker run hello-world
   ```
   This command runs a simple container that displays a "Hello World" message.

2. **List Running Containers**
   ```bash
   docker ps
   ```
   This command shows all currently running containers.

3. **Stop a Container**
   ```bash
   docker stop <container_id>
   ```
   Replace `<container_id>` with the ID or name of the container you want to stop.

4. **Remove a Container**
   ```bash
   docker rm <container_id>
   ```
   This command removes a stopped container from your system.

5. **List All Images**
   ```bash
   docker images
   ```
   This command lists all Docker images stored locally.

6. **Pull an Image**
   ```bash
   docker pull ubuntu
   ```
   This command downloads the latest Ubuntu image from the Docker Hub.

7. **Build an Image**
   ```bash
   docker build -t my-image:latest .
   ```
   This command builds a Docker image from a Dockerfile located in the current directory, tagging it as `my-image:latest`.

## Tips
- Always use specific tags for images to avoid pulling the latest version unintentionally, which may introduce breaking changes.
- Regularly clean up unused containers and images with `docker system prune` to free up space.
- Use Docker Compose for managing multi-container applications, as it simplifies the process of defining and running multiple containers.