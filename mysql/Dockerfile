# Use the official Ubuntu 20.04 LTS image as the base image
FROM ubuntu:20.04

# Set environment variables to configure MySQL
ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_DATABASE=my_database
ENV MYSQL_USER=argisht
ENV MYSQL_PASSWORD=password

# Install MySQL server
RUN apt-get update && \
    DEBIAN_FRONTEND="noninteractive" apt-get install -y mysql-server && \
    rm -rf /var/lib/apt/lists/*

# Start MySQL service on container startup
CMD ["mysqld", "--user=mysql", "--console"]
