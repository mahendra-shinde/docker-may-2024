# Building Images using Dockefile 

1. Dockerfile
   
   A Simple document that should `describe` all the steps for building an image.

   > Dockerfile Syntax
   ```dockefile
   INSTRUCTION ARGUMENT1 ARGUMENT2   ARGUMENT-N
   INSTRUCTION [ ARG1, ARG2, ARG3 ... ARG-N ]
   ```

    - The filename Must be `Dockerfile` (It is case-sensitive)
    - File must be placed on root-level.

    
- Project Directory Structure (1)

    ```
    - Root folder
      ---> src
        --> Solution or Project
      ---> Dockerfile
      ---> .dockerignore
    ```

- Project Directory Structure (2)

    ```
    - Root folder
      --> Solution or Project
      ---> Dockerfile
      ---> .dockerignore
    ```