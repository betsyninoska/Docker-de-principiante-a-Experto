FROM  nginx

RUN yum -y update

RUN yum -y install httpd httpd-tools


ADD starbootstrap-freelancer-master /var/www/html
CMD apachectl -DFOREGROUNG
