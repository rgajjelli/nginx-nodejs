# Set nginx base image
FROM nginx


# Remove the default Nginx configuration file
RUN rm -v /etc/nginx/nginx.conf

# Copy custom configuration file from the current directory
COPY nginx.conf /etc/nginx/nginx.conf

# Append "daemon off;" to the configuration file
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

RUN mkdir -p /var/www/public
ADD web/src/index.html /var/www/public

# Expose ports
EXPOSE 88

# Set the default command to execute when creating a new container
CMD service nginx start
