FROM ubuntu


# Install Nginx

# Add application repository URL to the default sources
#RUN echo "deb http://archive.ubuntu.com/ubuntu/ raring main universe" >> /etc/apt/sources.list

# Update the repository
RUN apt-get update

# Install necessary tools
RUN apt-get install -y nano wget dialog net-tools

# Download and Install Nginx
RUN apt-get install -y nginx  

RUN mkdir -p /etc/nginx/certs/

# Remove the default Nginx configuration file
#RUN rm -v /etc/nginx/conf.d/nginx.conf

# Copy a configuration file from the current directory
ADD nginx.conf /etc/nginx/
ADD ./files/* /etc/nginx/certs/

# Append "daemon off;" to the beginning of the configuration
#RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80
EXPOSE 443

# Set the default command to execute
# when creating a new container
#CMD service nginx start
CMD ["nginx", "-g", "daemon off;"]
