# Docker 🐳

Note-taking repository for Docker. 

## Why use Docker ?

- Compatibility/Dependency
- Different dev/test/prod environments
- Long setup time

## What can Docker do ?

- Containerize applications
- Run each service with its own dependencies/libraries in separate containers

## What are containers ?

- Containers are **completely isolated environments**
- Containers have their own processes, services, network interfaces, mounts, etc..
- Containers share the same OS kernel

*Docker, which launched in 2013, initially utilized LXC to provide an easier way to create, deploy, and run applications using containers.  Docker quickly evolved from using LXC as its default execution environment by developing its own container runtime, ```libcontainer```, which now powers Docker containers.*