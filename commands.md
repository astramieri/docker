# Docker Commands

## ```run``` (start a container)

The docker ```run``` command is used to run a container from an image. Each container gets a random ID and name.

    > docker run <image>

If the image is not present on the host, the image is downloaded from Docker Hub. This is only done the first time, fort the subsequent executions the same image will be reused.

## ```ps``` (list containers)

The docker ```ps``` lists all running containers with some basic information about them.

    > docker ps

