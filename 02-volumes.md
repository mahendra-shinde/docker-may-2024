# Volumes

1. A Single container can have ZERO or MORE volumes
1. A Volume could be SHARED between multiple containers
1. Volumes are  `Persistent storage`, are retained after containers are deleted.

# Kind of Volumes

1. Named (Managed) Volumes
    Create a volume : `docker volume create NAME`

    Attach volume to NEW container: `docker run [..OPTIONS...] -v VolName:/Guest/Path/ IMAGE`

    Delete a volume : `docker volume rm NAME`

2. Host Path Volumes (Ad-Hoc Volumes)

    Attach existing "Local" directory as volume to container

    `docker run [...OPTIONS...] -v C:\Host\Path:/Guest/Path IMAGE`

# Mount Options

-v VolName:/Guest/Path:RO   --> Read Only Volume
-v VolName:/Guest/Path:RW   --> Read/Write (Default)

## Try Hosted Path

1. Create a new local folder

    mkdir c:\webapp

2.  Create a new container for DOTNET-SDK and use C:\webapp as host-path volume

    ```
    docker run --name w4 -it -v c:\webapp\:/app   mcr.microsoft.com/dotnet/sdk:6.0-jammy bash
    cd /app
    dotnet new webapp -n app1
    cd app1
    dotnet build 
    exit
    ```

3.  Open C:\webapp in file explorer and verify the asp.net project 'app1' created !