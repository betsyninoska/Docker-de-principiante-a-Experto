FROM nginx

LABEL version=1.0

RUN useradd betsy

COPY  theme  /usr/share/nginx/html

ENV archivo docker

WORKDIR /usr/shared/nginx/html

RUN echo "$archivo"> /usr/shared/nginx/html/env.html

EXPOSE 90


USER betsy

RUN echo "$(whoami)" > /tmp/yo.html

USER root

RUN cp /tmp/yo.html /usr/shared/nginx/html/docker.html

VOLUME /var/log/nginx


CMD nginx -g 'daemon off;'
