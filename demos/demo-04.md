# Network demo

1. Create a new network

    `docker network create net1 --subnet 10.0.10.0/24`

1. Launch TWO containers in this network

    ```
    docker run --name w1 --net net1 -d nginx:alpine
    docker run --name w2 --net net1 -d nginx:alpine
    ```

1.  Get the Container IPs

    ```
    docker exec -it w1 hostname -i
    docker exec -it w2 hostname -i

    docker network inspect net1
    ```

1.  Test the connectivity between containers 

    ```
    docker exec -it w1 ping w2
    ## PRESS CTRL+C
    docker exec -it w2 ping w1
    ## PRESS CTRL+C
    ```

1.  Create a new container `outside` network net1

    ```
    docker run --name w3 -d nginx:alpine
    docker exec -it w1 ping w3
    ## FAIL : Bad Address
    ```

1.  Attach container `w3` to network `net1`

    ```
    docker network connect net1 w3
    docker exec -it w1 ping w3
    ## Success !
    ## PRESS CTRL+C
    ```

1.  Clean Up

    ```
    docker stop w1 w2 w3
    docker rm w1 w2 w3
    docker network rm net1
    ```