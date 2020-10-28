FROM centos:7
MAINTAINER Dmitriy Mosk <erzhick10@gmail.com>
RUN yum install -y epel-release && yum install -y nginx
RUN yum clean all
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
RUN sed -i "0,/nginx/s/nginx/docker-nginx/i" /usr/share/nginx/html/index.html
CMD [ "nginx" ]

#FROM ubuntu

#RUN apk add --no-cache curl wget busybox-extras netcat-openbsd python py-pip && \
#    pip install awscli
#RUN apk --purge -v del py-pip
#CMD tail -f /dev/null
