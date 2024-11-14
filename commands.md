# Docker commands

- [```version```](./command_version.md) 
- [```images```](./command_images.md) 
- [```pull```](./command_pull.md) 
- [```ps```](./command_ps.md) 
- [```run```](./command_run.md) 



## ```stop```

This command is used to stop a container. You must provide either the *container ID* or the *container name*.

    > docker stop <container>

## ```rm```

This command is used to remove a stopped or exited container permanently.

    > docker rm <container>

## ```rmi```

This command is used to remove an image that you no longer plan to use. You must stop and delete all dependent containers to be able to delete an image.

    > docker rmi <image>

## ```exec```

This command is used to execute a command on a Docker container.

    > docker exec <container> cat /etc/hosts

## ```attach```

This command is used to attach to a detached running container.

    > docker attach <container>