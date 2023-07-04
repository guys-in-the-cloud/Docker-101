# Docker Day-3
---
## Docker Registry:
A Docker registry is a centralized storage location that holds Docker images. It is a service that allows you to store, manage, and distribute Docker images.
Example:- Docker hub, ECR(Elastic Container Registry, GCR(Google Container Registry) etc

## Docker Repository:
A Docker repository is a collection of related Docker images with different tags. When you push a Docker image to a registry, it is stored in a repository. The repository is like a catalog that contains multiple versions (tags) of the same Docker image.

## Docker Images:
A Docker image is a lightweight, standalone, and executable software package that includes everything needed to run a piece of software, including the code, runtime, libraries, environment variables, and system tools. It is essentially a snapshot of a file system that contains an application and all its dependencies.
### Synatx of Docker image
```
[REGISTRY_HOST]/[REPOSITORY_NAME]:[TAG]
```
Example:
```
gaurav0408/pythonimage:1
```
* gaurav0408 is Registry(Dockerhub Username) </br>
* pythonimage is Repository Name </br>
* 1 is 1st version of our image
### Images Commands:
1. docker pull: The docker pull command is used to pull Docker images from a container registry onto your local system. To use this command, you need to specify the name of the image you want to pull, typically in the format "registry/repository:tag". If the tag is omitted, the latest tag is assumed by default.
```
docker pull hello-world
```
<p align="center">
  <img width="620" alt="docker images" src="https://github.com/gauravrattan/Docker-101/assets/100664099/a2cbd8e8-66c6-43b2-bfd8-e6f0122d0a85">
</p>

If a Docker image is not locally present on your system, Docker will automatically try to fetch the image from the specified registry 
(e.g., Docker Hub) in the form of Layers(Images are composed of multiple layers).hello-world is the name of the image someone created on dockerhub for us. It will first search for “hello-world” image locally and then search in Dockerhub.

2. List the images:
```
docker images
```

<p align="center">
<img width="464" alt="Screenshot 2023-07-05 at 12 03 42 AM" src="https://github.com/gauravrattan/Docker-101/assets/100664099/a5807493-3b92-44e0-b81b-3b73f8abc99e">
</p>
  
This will display a list of Docker images that are present on your system

3. list of image ID:
   ```
   docker images -q
   ```
<p align="center">  
  <img width="354" alt="imagesID" src="https://github.com/gauravrattan/Docker-101/assets/100664099/bea03576-d067-4984-8c26-c81ce2642ca1">
</p>

The docker image -q command is used to list the image IDs of all the Docker images present on your system. It's a shorthand for listing only the image IDs without any additional details such as repository names, tags, or sizes.


