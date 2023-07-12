FROM centos:7	
LABEL version=1.0
LABEL descripción= 'This is an apache images'
LABEL  vendor='Betsy'	

RUN yum install htppd -y
COPY  starbootstrap-freelancer-master /var/www/html
RUN echo "$(whoami)"> /var/www/html/user1.html
RUN useradd betsy
RUN echo "$(whoami) > /tmp/user2.html"
USER root 
RUN cp /tmp/user2.html /var/www/html/user2.html
COPY run.sh /run.sh

CMD sh /run.sh
