FROM ubuntu

# Update the repository
RUN apt-get update

# Download and Install Nginx
RUN apt-get install -y nginx  

# Create directory to copy certs to
RUN mkdir -p /etc/certs


# Copy a configuration file from the current directory
ADD nginx.conf /etc/nginx/
ADD ./files/* /etc/certs/

# Set the default command to execute
# when creating a new container
CMD ["nginx", "-g", "daemon off;"]
