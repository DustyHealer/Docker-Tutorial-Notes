# Docker commands avaialabe for execution

## docker run: 
1. Check for image in the docker cache. 
2. If not present, it downloads the docker image file system snapshot from the docker hub. 
3. After that it fires the startup command.
4. We can override the startup command also. Examples docker run hello-world ls, docker run hello-world sh, docker run hello-world echo himanshu singhal.
5. docker run = docker create + docker start.
6. docker create = creates a container and displays the hashcode on the terminal screen.
7. docker start -a container_hash: Will start the container and display the result on terminal.
8. docker start container_hash: Will not print the output of the container, instead prints the hash code.

# List all docker containers
docker ps: List all the currently running containers.
docker ps -a or docker ps --all: This command list all the containers whether they are running, paused or exited.

docker logs container_id: To check the logs for a particular container.

# Remove containers
docker stop container_id: This command will stop the container with id = container_id.
docker kill container_id: This command will kill containers just like we kill processes in task manager. Mostly used for unresponsive processes or containers. 

# docker exec
docker exec -i -t container_id ls: To run commands inside the docker container. In this case, we are running the ls inside the container. We can start the terminal inside the container inside the sh.

# Docker File

Docker file contains all the info for running your software in a base container.

Process of docker file to image:
Docker File(Plain Text) ----> Docker Client ----> Docker Server ----> Usable Image

How to create a custom image:
1. Choose a base image.
2. Run commands for your software.
3. Specify the base command to be ran at the startup.

# Image Tagging
docker build -t himanshu(docker username)/redis(image name):latest(version) .(dot)

# Run docker image on the machine instead of virtual machine
1. When we install a image inside a docker container, it is running inside the VM which can not be directly accessed by the machine IP.
2. In order to do this, we need to map the port of the local machine to the port inside docker container. Then we can access the software running inside the docker container.
3. Command which is used for this purpose: docker run -p 80(local machine port):80(docker machine port) nginx(image name)