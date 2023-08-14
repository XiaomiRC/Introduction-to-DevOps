Docker Installation and some important commands

1. Create an EC2 on AWS with Docker installed AMI. If not installed, run the command:
```
yum install docker -y
```
2. View all the images available locally
```
docker images
```
3. Search for images on the Docker Hub
```
docker search image-name
```
4. Downlload an image from Docker Hub to your local machine
```
docker pull image-name
```
5. Give a name to the container and run it.
```
docker run -it --name container-name imagename /bin/bash
```
6. To check whether the service has started
```
service docker status
```
OR
```
service docker info
```
7. To start the service
```
service docker start
```
8. Start/Stop a container
```
docker start container-name
```
```
docker stop container-name
```
9. to get inside the container
```
docker attach container-name
```
10. View all containers
```
docker ps -a
```
11. View only the running containers
```
docker ps
```
12. Delete a container
```
docker rm container-name
```
13. Exiting from a container
```
exit
```
14. To delete an image
```
docker image rm image-name
```
