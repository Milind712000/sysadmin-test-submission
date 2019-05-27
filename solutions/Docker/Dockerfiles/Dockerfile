FROM ubuntu:bionic
RUN apt update -y
RUN apt install apache2 apache2-utils curl -y
COPY ./index.html /var/www/html
CMD apache2ctl -D BACKGROUND > /dev/null 2>&1 && curl -s localhost 
