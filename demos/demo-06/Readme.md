# Demo 6 : Build from "Scratch"

1. Make sure your folder hierarchy looks like :

    ```
    demo-06
        src\
            index.html
            main.css
        alpine-minirootfs-3.19.1-x86_64.tar.gz
        default.conf
    ```

1.  Using Command prompt or Powershell, build the image

    ```cmd
    cd demo-06
    docker build -t test1 . 
    docker images test1
    ```

1.  Test run 

    ```cmd
    docker run --name w1 -d -p 8000:80 test1
    start http://localhost:8000
    docker stop w1
    docker rm w1
    ```