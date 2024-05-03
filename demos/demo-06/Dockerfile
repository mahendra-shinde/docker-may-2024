# DO NOT USE ANY BASE IMAGE
FROM scratch

# Extract the contents of a  `LOCAL` tarball at ROOT directory "/"
# ADD can also download "single" file from a URL
ADD alpine-minirootfs-3.19.1-x86_64.tar.gz /

# Execute the COMMAND in "Temp" containers
RUN apk update && apk add nginx

## Use updated default config for NGINX
COPY default.conf /etc/nginx/http.d/default.conf

# Copy the Website
COPY src /usr/share/nginx/html/

# A Startup command
ENTRYPOINT [ "nginx","-g", "daemon off;" ]