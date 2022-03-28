# Base image
FROM ubuntu:16.04 

# Maintainer
MAINTAINER Amit <amitvashist7@outlook.com>

# Apt-Repo Update 
RUN apt-get update 

# Install Apache2 Packages 
RUN apt-get install apache2 -y 

# Bring Apache Service UP.
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
