Containers
- Wrappers for app and all its dependencies

Docker
- Container platform, which allows building and running containers

Container Runtimes:
- libcontainerd
- cri-o

Container Instances : Real instances that consume resources
Container Images    : Template for "instances"

Container Network : A Virtual network that can group multiple containers together

Network Drivers:
- Bridge [Default]  : Allow new network creation
- None (Null)       : Disable Networking
- Host (host)       : Direct connect with Local (Host)
 
Volumes
- Persistent storage which can be shared by containers
- Named volumes and Host Path Volumes
- Volumes are retained even after container are deleted