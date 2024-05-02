# Container Execution modes

1.  Terminal only (Read only) [Default]

    `docker --name w1 run -p 8000:80 nginx:alpine`

    > To Test, visit browser http://localhost:8000

1.  Interactive Terminal 

    `docker run --name w2 -it -p 8001:80 nginx:alpine`

    > To Test, visit browser http://localhost:8001

1.  Detached / Background mode

    `docker run --name w3 -d -p 8002:80 nginx:alpine`

    > To Test, visit browser http://localhost:8002

1.  Clean Up

    ```
    docker stop w1 w2 w3
    docker rm w1 w2 w3
    ```