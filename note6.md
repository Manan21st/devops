# Introduction to Docker and Containers

## What is Docker?
Docker is an open platform for developing, shipping, and running applications.  
It allows developers to separate applications from the underlying infrastructure, enabling faster and more reliable software delivery. With Docker, infrastructure can be managed in a similar way to application code.

---

## Running Applications in Containers
Containers allow applications to be packaged together with all required dependencies such as libraries and system tools.  
This approach ensures that applications run consistently across different environments, regardless of where they are deployed.

---

## Basic Docker Commands

### Running a Container
- **docker run**  
  Used to create and start a new container.  
  Example: `docker run -it ubuntu bash`
  This command starts an Ubuntu container and provides terminal access.

---

### Entering an Existing Container
- **docker exec**  
Used to execute commands inside an already running container.  
Example: `docker exec -it <container_id> bash`
This opens a terminal session inside the running container.

---

### Inspecting Docker Containers
- **docker ps**  
Lists all currently running containers.

- **docker container inspect <container_id>**  
Displays detailed information about a container, including its configuration and IP address.

---

## Working with Docker Images

### Creating and Managing Images
Docker images can be created by modifying an existing container and saving the changes.

- **docker images**  
Lists all available Docker images.

- **docker commit -m "" <container_id> <new_image_name>**  
Creates a new image from a container with the current state preserved.

---

### Pushing Images to Docker Hub
- **docker push <image_name>**  
Uploads an image to Docker Hub.

To successfully push an image, the image name must begin with the Docker Hub username.

---

## Networking and Container Communication
To allow communication between containers, it is often necessary to identify a container’s IP address.

- **docker container inspect <container_id>**  
Retrieves the IP address of a container.

Once the IP address is known, tools such as `curl` can be used to interact with services running inside the container.

---

## Dockerfile and Image Layers
Docker images are commonly created using a Dockerfile, which defines a sequence of steps to build the image.

Each instruction in a Dockerfile adds a new layer to the image.  
Understanding image layers is important for efficient image building and effective use of Docker’s caching mechanism.

---

## Practical Usage Concepts

### Detached vs Attached Modes
- **docker run -d**  
Runs a container in detached mode, meaning it runs in the background.

### Importance of Layered Filesystems
Each Docker image consists of multiple layers.  
When changes are made to a container and committed, a new layer is created that represents only those changes.

---

## Additional Insights
Docker improves efficiency when compared to virtual machines.  
Unlike virtual machines, Docker containers do not require a full operating system, as they use the host OS kernel.

In multi architecture environments, compatibility issues may arise, such as differences between ARM and AMD architectures.  
This highlights the importance of maintaining consistent architectures during image creation and deployment.

---

## Conclusion
Docker provides a powerful and flexible approach to developing, shipping, and running applications.  
It simplifies container management, supports efficient debugging, and enables reliable deployment in modern software development environments.


