# Docker Compose

- A Utility to manage multi-container applications.

## Commands

Sr No | Command | Description
-----|-----|-------
1 | docker-compose config | Validate the 'compose' file
2 | docker-compose pull   | Download all the images referred in 'compose' file
3 | docker-compose up -d  | Create and Start Network, Volumes and Containers
4 | docker-compose down   | Stop and delete network and containers
5 | docker-compose ps     | List all the containers from CURRENT compose file
6 | docker-compose stop   | Stop the containers
7 | docker-compose restart | Restart all the containers
8 | docker-compose logs  SERVICENAME | print logs for given service


## Syntax for docker-compose

* Valid names for compose file

    1. docker-compose.yaml
    2. docker-compose.yml
    3. compose.yaml
    4. compose.yml

* Syntax

```yaml
version: '3.7'

services:
  service_a:
  
  service_b:

# Volumes are OPTIONAL
volumes:
   vol1:
   
   vol2:

# Networks are OPTIONAL
# When MISSING, docker would create a "default" network
networks:
   net1:
   
   net2:
```