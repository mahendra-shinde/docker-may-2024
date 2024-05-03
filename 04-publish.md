# Publish images to Registry

- Local images must be PUBLISHED to a remote repository.

## Steps 

1. You must LOG-IN into remote registry from Docker CLI

    > Login into Docker Hub

    ```bash
    docker login -u [USERNAME] -p [PASSWORD/TOKEN]
    ```

    ```bash
    docker login -u mahendrshinde -p [PASSWORD/TOKEN]
    ```

    > Remote Registry  (Other than Docker Hub)

    ```bash
    docker login [REGISTRY-URL] -u [USERNAME] -p [PASSWORD/TOKEN]
    ```

    ```bash
    docker login mahendrashinde.azurecr.io -u mahendrashinde -p [PASSWORD/TOKEN]
    ```


1.  Re-Tag your local image, the new tag MUST USE registry-url as PREFIX. Then use "push"

    > When using Docker Hub (Default Registry)

    ```
    docker tag [localname] [username]/[localname]
    docker push [username]/[localname]
    ```

    ```
    docker tag test6 mahendrshinde/test6
    docker push mahendrshinde/test6
    ```

    > When using Other Registries (non-default)

    ```
    docker tag [loginserver-url] [loginserver-url]/[localname]
    docker push [loginserver-url]/[localname]
    ```

    ```
    docker tag test6 mahendrashinde.azurecr.io/test6
    docker push mahendrashinde.azurecr.io/test6
    ```

    