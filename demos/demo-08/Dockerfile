FROM ubuntu:latest

RUN apt update -y && apt install cowsay -y

ENTRYPOINT [ "/usr/games/cowsay" ]

## Argument to ENTRYPOINT
CMD ["Hello World"] 

## To Test
# docker run test1                      # Using default CMD from Dockerfile
# docker run test1 "Hello India"        # Override the CMD

### Incase, you dont want to use ONLY CMD
## CMD ["/usr/games/cowsay", "Hello World"]