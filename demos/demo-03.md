# Build a new image using `docker commit`

1. Launch a container `w1`

    ```
    docker run --name w1 -p 8000:80 -d mahendrshinde/myweb:1
    ```

1.  To Test application, use following URLs

    http://localhost:8000/              ---> Success
    http://localhost:8000/about.html    ---> 404 Error    


1.  To fix 404 error, lets `Get Inside` the running container

    ```
    docker exec -it w1 sh
    cd /usr/share/nginx/html 
    echo '<h2>About Us</h2>' > about.html
    exit
    ```

1.  Re-Test the URL

    http://localhost:8000/about.html    ---> Success

1.  Create `contact.html` using local VSCOde editor and then copy it inside the container

    ```
    docker cp contact.html w1:/usr/share/nginx/html/
    ```

1.  Test the URLs

    http://localhost:8000/contact.html    ---> Success

1.  Capture the container 'w1' and save it as new image

    ```
    docker commit w1 myweb:4
    docker stop w1
    docker rm w1
    docker run --name w1 -p 8000:80 -d myweb:4
    ```
1.  Test the URLs

    http://localhost:8000/contact.html    ---> Success

1.  Clean Up

    ```
    docker stop w1
    docker rm w1
    docker rmi myweb:4
    ```