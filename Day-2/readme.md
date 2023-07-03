# Docker Day-2
---
## Containerization:
Containerization is a technology that allows you to package an application along with all its dependencies, libraries, and configuration files into a single unit called a container. Containers provide a consistent and isolated environment for running applications, making them portable across different systems and eliminating potential conflicts between applications and their dependencies.

## Docker:
Docker is an open-source platform and a powerful tool for automating the deployment, scaling, and management of applications within containers. It allows developers to package applications and their dependencies into a container, ensuring they can run reliably and consistently on any environment, regardless of the underlying infrastructure.Docker is primarily known as a container runtime.
<p align="center">
  <img width="280" src= "https://github.com/gauravrattan/Docker-101/assets/100664099/cc18a2ea-972b-4ed2-bb9c-38c0241e045e" title="Docker">
</p>

## Docker Architecture:
Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface.
<p align="center">
  <img width="480" src= "https://github.com/gauravrattan/Docker-101/assets/100664099/744d5734-bb77-4316-bd33-91c0976752ae"  title="Docker Architecture">
 </p>

### 1. Docker Client:
The Docker Client is the primary interface through which users interact with Docker. It can be a command-line tool (docker CLI) or a graphical user interface (GUI). The Docker Client sends commands and requests to the Docker Daemon, which in turn manages containers and other Docker resources.

### 2. Docker Daemon: 
The Docker Daemon is the core background service that runs on the host machine. It is responsible for managing containers, images, volumes, networks, and other Docker resources. The Docker Daemon listens for API requests from the Docker Client and executes the necessary actions to create, start, stop, and manage containers.

### 3. Container Runtime: 
Docker Engine(Docker) utilizes a container runtime, such as containerd, to create and manage containers. The container runtime handles the low-level operations required to run containers, including container lifecycle management and isolation from the host system.

### 4.Docker Registries: 
Docker Registries are repositories that store and distribute Docker Images. Docker Hub is the default public registry provided by Docker, housing a vast collection of official and community-contributed images. Private registries can also be set up to store proprietary or sensitive images.

### 5. Docker objects 
It refer to the fundamental entities or components that Docker uses to enable containerization and manage containers and related resources. These objects are the building blocks of the Docker ecosystem and play a crucial role in the container lifecycle. Some of the key Docker objects include: Images, Containers, Network, Volume etc.

## Installation Of Docker:
1. Update the Machine:
```
sudo apt update
```
2. Install the docker package
```
sudo apt install docker.io -y
```
3. To run Docker commands without using sudo, you should add your user to the docker group and then log out and log back in or restart your system
```
sudo usermod -aG docker $USER
```
4. Check the version
```
docker --version
```
5. You can also check information of your Docker Server
```
docker info
```
