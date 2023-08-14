# Docker Short Notes
  
## Basics of Docker 

1. Docker was first released in March 2013. It was developed by Solomon Hykes and Sebastien Paul.
2. Docker is an open-source centralized platform designed to create, deploy and run applications.
3. Docker uses the container on the host OS to run applications. It allows applications to use the same Linux Kernal as a system on the host computer, 
rather than creating a whole virtual OS.
4. We can install Docker on any OS but the Docker engine runs natively on Linux distribution.
5. Docker is written in the 'GO' language.
6. Docker is a tool that performs OS-level virtualisation, also known as containerization.
7. Before Docker, many users had faced the problem where a particular code ran in the developer's system but not in the user's system.

## Advantages of Docker

1. No pre-allocation of RAM.
2. CI Efficiency - Docker enables us to build a container image and use that same image across every step of the deployment process.
3. Less Cost.
4. It is light in weight.
5. It can run a physical hardware, virtual hardware or on cloud.  
6. You can reuse an image.
7. It taks very less time to create another container.

## Disadvantages of Docker

1. Docker is not a good solution for application that requires a rich GUI.
2. It is difficult ot manage a large number of containers.
3. Docker does not provide cross-platform compatibility, meaning if an application is designed to run in a docker container on windows, then it can't run on Linux or vice-versa.
4. Docker is suitable when the development OS and testing OS re the same, if the OS are different, we should use VM.
5. Docker has no solution for data recovery and backup.

**Note**- When a docker image is in running state, we can call it a container. When it is not running, we can call it a docker image.


# Components of Docker 
## Docker Daemon 

1. Docker daemon runs on the host OS.
2. It is responsible for running containers, and managing docker services.
3. Docker daemons can communicate with other daemons.

## Docker Client

1. Docker users can interact with the docker daemon through a client. 
2. Docker client uses commands and Rest API to communicate with the docker daemon
3. When a client runs any server command on the docker client terminca, the client terminal sends the docker commands to the docker daemon.
4. Docker clients can communicate with more than one daemon.

## Docker Host

Docker Host is used for providing an environment to execute and run applications. It contains the docker daemon, images, containers, networks, and storage.

## Docker Hub/Registry
1. Docker registry manages and stores the docker images.
2. There are two types of registries in the docker.
i) Public Registry - It is also called Docker Hub.
ii) Private Registry - It is used to share images within the enterprise.

## Docker Images

Docker images are the read-only binary templates used to create docker containers OR a single file with all dependencies and configurations required to run a program.

### Ways to create an image

1. Take an image from Docker Hub.
2. Create an image from a Docker File.
3. Create an image from the existing Docker Containers.

## Docker Container

1. The container holds the entire package that is needed to run the application. In other words, we can say that the image is a template and the container is a copy of that template.
2. Container is like virtualization when they are run on the Docker Engine.
3. Images become containers when they run on the docker engine.

