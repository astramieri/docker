# Docker ```run``` command

The Docker ```run``` command is used to run a container from an image. Each container gets a random *ID* and *name*. 

If the image is not present on the host, the image is downloaded from Docker Hub. This is only done the first time, fort the subsequent executions the same image will be reused.

    > docker run <image>

Unlike VMs, containers are meant to run a specific task or process (e.g. host an instance of a web server). Once the task is complete, the container exits. **The container only lives as long as the process inside it is alive**. Is the process inside the container is stopped, or crash, then the container exists.

In the case with Ubuntu image, you could instruct Docker to run a process with the Docker run command.

    > docker run ubuntu              (exit immediately)

    > docker run ubuntu sleep 5      (exit after 5 seconds)

To stop a container, use ```CTRL-c```. This key sequence sends ```SIGKILL``` to the container.

## Attached VS Detached

When you run a container, it runs in the *foreground* or in **attached mode**, meaning you will be attached to the standard out of the Docker container. You won't be able to do anything else on this console other than view the output until this Docker container stops.

Another option is to run the Docker container in the **detached mode**. This will run the Docker container in the *background* mode and you will be back to your prompt immediately. The container will continue to run in the backend. If you would like to attach back to the running container later, use the ```attach``` command.

    > docker run <image>            (attached mode)

    > docker run -d <image>         (detached mode)
