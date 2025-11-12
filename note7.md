# Introduction to Docker

Docker is a platform that enables developers to automate the deployment, management, scaling, and operation of application containers.  
This session focused on understanding Docker fundamentals, including image creation, Dockerfiles, and commonly used commands for managing containers.

---

## Key Concepts Explained

### Docker Images and Containers

**Docker Image**  
A Docker image can be thought of as a packaged environment for an application.  
It contains everything required to run the application, including code, runtime, libraries, and dependencies. Docker images serve as the building blocks for containers.

**Docker Container**  
A Docker container is a running instance of a Docker image.  
It is similar to a virtual machine but much lighter, as it shares the host system kernel. This makes containers faster and more efficient than traditional virtual machines.

---

## Basic Commands and Usage

### Docker Build
The `docker build` command is used to create Docker images from a Dockerfile.  
It supports multiple options, such as `-t`, which assigns a name or tag to the image.  
Image tags should always be written in lowercase.

### Docker Run
The `docker run` command starts a container from a Docker image.  
Common options include:
- `-d` to run the container in detached mode  
- `-p` to map container ports to host ports  

---

## Dockerfile Essentials

A Dockerfile is a script that contains a sequence of instructions used to build a Docker image.

**FROM Command**  
Specifies the base image that serves as the starting point for the Docker image.

**RUN Command**  
Executes commands during the image build process.  
Each RUN instruction creates a new image layer, which can impact image size and performance if not optimized.

**CMD and ENTRYPOINT**  
Both define the default command executed when a container starts.
- `CMD` can be overridden by passing arguments during container startup.
- `ENTRYPOINT` is fixed and cannot be overridden in the same way.

---

## Advanced Concepts

### Multi Stage Builds
Multi stage builds help reduce the final image size by separating the build environment from the runtime environment.  
Only the necessary artifacts are copied into the final image, improving performance and efficiency.

### Copy On Write (CoW) Mechanism
Docker uses a copy on write mechanism to optimize performance.  
Only modified files are copied into a container’s writable layer, reducing memory usage and improving startup speed.

---

## Performance Optimization Strategies

### Reducing Layers
Minimizing the number of layers in a Docker image improves performance.  
This can be achieved by combining multiple commands into a single RUN instruction using logical operators like `&&`.

### Base Image Optimization
Choosing an appropriate base image significantly affects image size and container performance.  
For example, Java applications should use a JRE instead of a JDK in production environments to reduce image size.

---

## Practical Application and Example
A practical example discussed in class involved creating a Docker image for a Java application using a multi stage build.  
The build stage used a JDK to compile the application, while the final stage used a JRE to produce a lightweight production image.

---

## Tools and Environment
The session included guidance on setting up Docker environments, creating containers, and deploying applications.  
Hands on practice was emphasized to ensure a clear understanding of Docker commands and workflows.

---

## Conclusion
This class provided an in depth understanding of Docker, covering image creation, container execution, and performance optimization best practices.  
These concepts are essential for software engineers aiming to effectively use Docker in modern deployment pipelines.
