# Download the base image 'nginx:alpine'
FROM nginx:alpine

# Docker BuildKit would create a new "Temp" container
# then "Copy" the marked file into that container
# Capture the container into a new Temp Image
COPY index.html /usr/share/nginx/html/

# Create another Temp Container from Image created in LAST STEP !
# Copy the CSS file and capture the image
COPY main.css /usr/share/nginx/html/

# As this is END OF FILE
# Docker would now MARK the last image as FINAL one!