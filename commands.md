# Docker Commands

## ```run``` (start a container)

The docker ```run``` command is used to run a container from an image. Each container gets a random *ID* and *name*.

If the image is not present on the host, the image is downloaded from Docker Hub. This is only done the first time, fort the subsequent executions the same image will be reused.

    > docker run <image>

## ```ps``` (list containers)

The docker ```ps``` lists all running containers with some basic information about them.

    > docker ps             (list all running containers)

    > docker ps -a          (list all containers, running or not)

## ```stop``` (stop a container)

The docker ```stop``` command is used to stop a container. You must provide either the *container ID* or the *container name*.

    > docker stop <container>