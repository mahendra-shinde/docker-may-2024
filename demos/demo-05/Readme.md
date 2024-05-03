# Demo 5 : Dockerfile demo

1. Make sure your folder hierarchy looks like :

    ```
    demo-05 
      Dockerfile
      index.html
      main.css
    ```

1.  Using Command prompt or Powershell, build the image

    ```cmd
    cd demo-05
    docker build -t myweb:5 . 
    docker images myweb:5
    ```

1.  Test run 

    ```cmd
    docker run --name w1 -d -p 8000:80 myweb:5
    start http://localhost:8000
    docker stop w1
    docker rm w1
    ```