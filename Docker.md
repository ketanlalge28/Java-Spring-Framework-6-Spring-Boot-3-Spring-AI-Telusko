# Docker

### Check Docker Version

```bash
docker --version
```

### Run a Test Container
Run a test container using the hello-world image to verify Docker installation.

```bash
docker run hello-world
```

### Pull a Docker Image
Pull the hello-world image from Docker Hub.

```bash
docker pull hello-world
```

### Check running containers
To show all currently running containers.

```bash
docker ps
```

### Check all containers
Show all containers, both running and stopped.

```bash
docker ps -a
```

### List available images
List all Docker images downloaded and available locally.

```bash
docker images
```

# Docker Commands

This document provides a list of basic Docker CLI commands used in the lecture.

### Common Docker Commands

| Command             | Description                                       |
|---------------------|---------------------------------------------------|
| `docker run`        | Create and run a new container from an image     |
| `docker exec`       | Execute a command in a running container         |
| `docker ps`         | List running containers                          |
| `docker ps -a`      | List all containers (running and stopped)        |
| `docker build`      | Build an image from a Dockerfile                 |
| `docker bake`       | Build from a file                                |
| `docker pull`       | Download an image from a registry                |
| `docker push`       | Upload an image to a registry                    |
| `docker images`     | List all downloaded Docker images                |
| `docker login`      | Authenticate to a Docker registry                |
| `docker logout`     | Logout from a Docker registry                    |
| `docker search`     | Search Docker Hub for images                     |
| `docker version`    | Show Docker version info                         |
| `docker info`       | Display system-wide Docker info                  |


### Container & Image Lifecycle Commands

**List All Containers**

```bash
docker ps -a
```

**Delete a container**

```bash
docker rm <container_id>
```

**List All Images**

```bash
docker images
```
**Delete an image**

```bash
docker rmi <image_id>
```


### Key Note:

- Every time you run a Docker container, a **new container ID** is generated.
- A container must be **removed first** before its corresponding image can be deleted.


### Step-by-Step: Docker Workflow
**1. Search for Images on Docker Hub**

```bash
docker search <image_name>
```

**2. Pull an image from Docker Hub**

```bash
docker pull <image_name>
```

**3. Check Containers (None Created Yet)**

```bash
docker ps -a
```

**4. Create a Container from the Image**

```bash
docker create <image_name>
```

**5. Verify Container is Created**

```bash
docker ps -a
```

**6. Start the Container**

```bash
docker start <container_id>
```
> Either the `container_id` or the `container_name` can be used.

**7. Confirm Container is Running**

```bash
docker ps -a
```

**8. Pause the Container (Optional)**

```bash
docker pause <container_id>
```

**9. Stop the container**

```bash
docker stop <container_id>
```

**10. Remove the container**

```bash
docker rm <container_id>
```

**11. Verify Container is Removed**
```bash
docker ps -a 
```

# Running SpringBoot App on Docker

This document provides a list of basic Docker CLI commands used in the lecture.

### Check Running Containers

```bash
docker ps
```

### List All Files in the Container (JDK Environment)

```bash
docker exec <container_name> ls -a
```
> Lists all folders and files in the container's root directory.

### Check Contents of /tmp Directory

```bash
docker exec <container_name> ls /tmp
```
> It will contain only one file in /tmp at the initial stage.


###  Copy the Spring Boot JAR File into the Container

```bash
docker cp target/rest-demo.jar <container_name>:/tmp
```
> This copies the `rest-demo.jar` into the container’s /tmp directory.


### Verify the JAR File is Present

```bash
docker exec <container_name> ls /tmp
```
> The `rest-demo.jar` file will be available in addition to the existing content.


###  Commit the Container to Create a New Docker Image

```bash
docker commit <container_name> ketan/rest-demo:v1
```
> Creates a new Docker image named `ketan/rest-demo` with tag `v1` from the current container state.


### List Docker Images

```bash
docker images
```
> Verifies that `ketan/rest-demo:v1` image has been created successfully.


### Default Behavior: JShell

When running ketan/rest-demo:v1, the container defaults to JShell:

```bash
docker run ketan/rest-demo:v1
```


### Set Default Command to Run JAR Using --change

To override the default JShell behavior, the `--change` flag is used while committing:

```bash
docker commit --change='CMD ["java", "-jar", "/tmp/rest-demo.jar"]' <container_name> ketan/rest-demo:v2
```
> This sets the default command to run the JAR directly when the image is run.


### Run the Updated Image (v2)

```bash
docker run ketan/rest-demo:v2
```
> This will now run the Spring Boot application from the JAR instead of entering JShell.


### Map Ports While Running the Container

```bash
docker run -p 8080:8080 ketan/rest-demo:v2
```
> Maps port `8080` of the container to `8080` on the host machine.

# Running First Container

### Build the Docker Image

Navigate to the directory that contains your `Dockerfile` and run:

```bash
docker build -t telusko/rest-demo:v3 .
```
> This builds a Docker image named telusko/rest-demo with tag v3 using the current directory (.) as the build context.


### List Available Docker Images
```bash
docker images
```


### Run the Docker Image with Port Mapping
```bash
docker run -p 8081:8081 telusko/rest-demo:v3
```
> This runs the container from the newly built image and maps port 8081 of the host to port 8081 of the container.
