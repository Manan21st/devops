# Introduction to Docker

## What is Docker?
Docker is a platform used for creating, running, and managing containers.  
It allows developers to package an application along with all its dependencies into a standardized unit called a container. This ensures that the application runs consistently across different environments.

---

## Docker Philosophy

### If It Fits, It Ships
A core philosophy of Docker is “if it fits, it ships”.  
This means that once an application is successfully packaged into a Docker container, it can be deployed on any system that supports Docker without additional configuration.

The developer’s main responsibility is to ensure that the application works correctly inside the container.

---

## Key Concepts in Docker

### Containers
Containers are lightweight, portable, and self contained units that include everything required to run an application, such as:
- Application code  
- Runtime environment  
- System tools  
- Libraries and dependencies  

Containers are similar to virtual machines but are more efficient because they share the host operating system kernel while remaining isolated at the user level.

---

### Images
Docker images are read only templates used to create containers.  
An image contains the application code and all required dependencies and serves as the blueprint for containers.

---

### Docker Daemon and Docker Client

**Docker Daemon**  
The Docker daemon is a background service that runs on the host system.  
It listens for Docker API requests and manages Docker objects such as containers, images, networks, and volumes.

**Docker Client**  
The Docker client is a command line interface used to interact with the Docker daemon.  
The client and daemon may run on the same machine, or the client can connect to a remote Docker daemon.

---

### Volumes and Networking

**Volumes**  
Volumes provide persistent storage for containers.  
They are used to store data that should survive container restarts or deletion and should not be stored inside the container’s writable layer.

**Networking**  
Docker provides built in networking features that allow containers to communicate with each other and with non Docker applications.

---

## Working with Docker

### Running Docker Containers
Containers are started using the `docker run` command.  
This command creates and starts a new container from a specified image.

Common flags include:
- `-i` for interactive mode  
- `-t` for terminal access  

These flags allow users to access a shell inside the running container.

---

### Docker Hub Repository
Docker Hub is a cloud based registry where users can store, share, and download Docker images.  
It acts as the default image repository when pulling images using Docker commands.

---

## Examples and Exercises
The class included hands on exercises where Docker containers were created and managed using Cloud Shell.  
These exercises focused on understanding Docker commands, image creation, and container deployment.

---

## Conclusion
Although Docker usage in large scale production environments has reduced due to container orchestration platforms like Kubernetes, Docker remains a fundamental tool for learning containerization concepts.

It provides a strong foundation for understanding advanced container management and orchestration technologies.

---

This concludes the introduction to Docker and its core concepts.
