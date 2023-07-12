FROM centos:7
LABEL version=1.0
LABEL descripcion='This is an apache images'
LABEL vendor=yo



RUN yum -y update

RUN yum -y install httpd httpd-tools

COPY  plantilla  /var/www/html

RUN echo "$(whoami)"> /var/www/html/user1.html

RUN useradd betsy

USER betsy

RUN echo "$(whoami)" > /tmp/user2.html

USER root

RUN cp /tmp/user2.html /var/www/html/user2.html

COPY run.sh /run.sh

CMD sh /run.sh
