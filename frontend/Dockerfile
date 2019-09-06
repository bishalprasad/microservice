#This is a docker file for microservice frontend layer
FROM centos:7
MAINTAINER prasad.bishal@gmail.com
RUN yum -y update
RUN yum -y install httpd
ADD config /opt
RUN yum -y install `cat /opt/packages`
RUN yum -y install `cat /opt/myapp-packages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test 
ADD script /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]
