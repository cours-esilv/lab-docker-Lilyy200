FROM nginx:alpine

# Install bash
RUN apk add --no-cache bash

# Set the environment variable for the backend URL
ENV WS_BACK_URL http://backend-service:5000

# Copy the entrypoint script into the image and make sure it's executable
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

# Copy your static web content to the nginx html directory
COPY . /usr/share/nginx/html

# Nginx listens on port 80 by default
EXPOSE 80

# Specify the entrypoint script to run
ENTRYPOINT ["/entrypoint.sh"]