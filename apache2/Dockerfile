FROM ubuntu:14.04
 
MAINTAINER Kevin Taron <kevin.taron@gmail.com>
 
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y apache2
 
RUN mkdir -p /data/apache/www
RUN chown -R root:www-data /data/apache/www
 
VOLUME /data/apache/www
 
EXPOSE 80
 
RUN sed -i 's#DocumentRoot /var/www#DocumentRoot /data/apache/www#' /etc/apache2/sites-available/000-default.conf
 
ENTRYPOINT /usr/sbin/apache2ctl -D FOREGROUND
 

Related Posts: