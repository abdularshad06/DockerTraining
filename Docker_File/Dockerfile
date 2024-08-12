# This is a sample image

# Define the base image on which we are going to customize

FROM ubuntu

# Define the maintainer and creator of this image

MAINTAINER Abdul Arshad <abdularshad390@gmail.com>

# Run the command to install apache as prerequisite

RUN apt-get -y update
RUN apt-get install -y apache2

RUN apt-get install -y apache2-utils
RUN apt-get update -y
RUN apt-get clean

# Exposing our application to a port
EXPOSE 80

#Copy the file from current host directory to the container

WORKDIR /var/www/html
COPY index.html /var/www/html/index.html

# The default command and command to start application in container
CMD [ "/usr/sbin/apache2", "-D", "FOREGROUND" ]

