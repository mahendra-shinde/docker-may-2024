# Demo 1 : Run a container

1. Launch a new container with ALL default options

    ```bash
    docker run mahendrshinde/cowsay
    ```

    > Docker would launch a new container with Auto-assigned name

2. Launch another new instance with `User defined name`

    ```bash
    docker run --name c1 mahendrshinde/cowsay
    ```

3.  List all the Containers

    ```bash
    docker ps -a
    ```

    > Expected : Two containers, one with name "c1"


4.  Launch third container in `Background`


    ```bash
    docker run --name c3 -d mahendrshinde/cowsay
    ```

    > Expected : No output from container, use `docker logs c3`

5.  Delete the stopped containers

    ```
    docker rm c1 c3
    --OR--
    docker container prune
    ```

6.  Delete the unused image

    ```
    docker rmi mahendrshinde/cowsay
    ```

    > ON deletion, images are first UNTAGGED, then docker would check if any other image is using layers from this image, all the shared layers are SKIPPED, but unique layers would be DELETED