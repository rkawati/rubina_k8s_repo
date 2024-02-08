# Use the official Ubuntu base imag
FROM ubuntu:latest

# Install Apache HTTP server
RUN apt-get update && \
    apt-get install -y apache2 && \
    rm -rf /var/lib/apt/lists/*

#Copy apache2.conf
COPY apache2.conf /etc/apache2/apache2.conf

# Set the environment variable for AWSECR
ENV ENV_NAME=AWSECR

# Add content to index.html
RUN echo "I am from ECR" > /var/www/html/index.html

# Expose port 80
EXPOSE 80

# Start the HTTP service using ENTRYPOINT
ENTRYPOINT ["apache2ctl", "-D", "FOREGROUND"]
Collapse
has context menu
