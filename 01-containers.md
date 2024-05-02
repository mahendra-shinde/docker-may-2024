# Containers

- Containers are `Generic Wrappers` for an applications. 

- Inside `A Container`, you package application binary, all its dependencies, required language runtime, server runtime and few OS Libraries.

- The command to launch a container is SAME, irrespective of programming language.

    ```
    docker run --name c1 -p 8080:80 -d mahendrshinde/myweb:1
    ```

    ```ini
    docker run  :  Command to launch a new container `instance` 
    --name c1   :  Logical name for new container [Optional]
    -p 8080:80  :  Port Forwarding, forward all traffic from Host port 8080 to container port 80
    - d         :  Detached mode (Run in background) 
    mahendrshinde/myweb:1   : Image name
    ```

## Basic Docker Commands

Sr No   | Command | Description
-------|----------|------------
1 | docker info | Print information about current docker engine
2 | docker version | Print docker version
3 | docker pull `[IMAGE]`| Download image from registry
4 | docker stop `[CONTAINER-NAME]` | Stop a running container(s)
5 | docker rm `[CONTAINER-NAME]` | Delete the containers
6 | docker run | Launch a new container
7 | docker ps | List all RUNNING containers
8 | docker ps -a | List All the containers including 'stopped' and 'running'

