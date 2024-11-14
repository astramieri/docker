# Docker commands

## ```version```

This command is used to print the current version number for all independently versioned Docker components.

    > docker version

## ```images```

This command is used to list all available images and their sizes.

    > docker images

## ```run```

This command is used to run a container from an image. Each container gets a random *ID* and *name*.

If the image is not present on the host, the image is downloaded from Docker Hub. This is only done the first time, fort the subsequent executions the same image will be reused.

    > docker run <image>

Unlike VMs, containers are meant to run a specific task or process (e.g. host an instance of a web server). Once the task is complete, the container exits. **The container only lives as long as the process inside it is alive**. Is the process inside the container is stopped, or crash, then the container exists.

In the case with Ubuntu image, you could instruct Docker to run a process with the Docker run command.

    > docker run ubuntu              (exit immediately)

    > docker run ubuntu sleep 5      (exit after 5 seconds)

When you run a container, it runs in the *foreground* or in **attached mode**, meaning you will be attached to the standard out of the Docker container. You won't be able to do anything else on this console other than view the output until this Docker container stops.

Another option is to run the Docker container in the **detached mode**. This will run the Docker container in the *background* mode and you will be back to your prompt immediately. The container will continue to run in the backend. If you would like to attach back to the running container later, use the ```attach``` command.

    > docker run <image>            (attached mode)

    > docker run -d <image>         (detached mode)

To stop a container, use ```CTRL-c```. This key sequence sends ```SIGKILL``` to the container.

## ```ps```

This command is used to list all running containers with some basic information about them.

    > docker ps             (list all running containers)

    > docker ps -a          (list all containers, running or not)

## ```stop```

This command is used to stop a container. You must provide either the *container ID* or the *container name*.

    > docker stop <container>

## ```rm```

This command is used to remove a stopped or exited container permanently.

    > docker rm <container>

## ```rmi```

This command is used to remove an image that you no longer plan to use. You must stop and delete all dependent containers to be able to delete an image.

    > docker rmi <image>

## ```pull```

This command is used to download an image.

    > docker pull <image>

## ```exec```

This command is used to execute a command on a Docker container.

    > docker exec <container> cat /etc/hosts

## ```attach```

This command is used to attach to a detached running container.

    > docker attach <container>