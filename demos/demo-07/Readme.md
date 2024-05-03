# Demo 5 : Dockerfile demo

1. Switch to `Windows Container` mode from the `Taskbar` icon of `Docker desktop`

1. Make sure your folder hierarchy looks like :

    ```
    demo-07
      Dockerfile
      index.html
      main.css
    ```

1.  Using Command prompt or Powershell, build the image

    ```cmd
    cd demo-07
    docker build -t wintest1 . 
    docker images wintest1
    ```

1.  Test run 

    ```cmd
    docker run --name w1 -d -p 8000:80 wintest1
    start http://localhost:8000
    docker stop w1
    docker rm w1
    ```