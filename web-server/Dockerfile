FROM ubuntu
MAINTAINER webalorn <webalorn@gmail.com>

RUN apt-get update && \
	apt-get install -y apache2 php libapache2-mod-php php-mysql

RUN a2enmod rewrite && \
 	rm -R /etc/apache2/sites-enabled && \
 	mkdir /etc/apache2/sites-enabled

# COPY root_files /

WORKDIR /data
EXPOSE 80