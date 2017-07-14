FROM centos:latest
RUN yum -y update && \
    yum -y install httpd php
EXPOSE 80
CMD ["/usr/sbin/httpd","-D","FOREGROUND"]
