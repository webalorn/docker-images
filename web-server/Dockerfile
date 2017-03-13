FROM php:apache
MAINTAINER webalorn <webalorn@gmail.com>

COPY root_files /

RUN rm -R /etc/apache2/sites-enabled && \
	mkdir /etc/apache2/sites-enabled && \

	# add custom script to entry point, before starting apache2
	echo "" >> /usr/local/bin/custom-server-entrypoint && \
	cat /usr/local/bin/docker-php-entrypoint >> /usr/local/bin/custom-server-entrypoint && \
	cat /usr/local/bin/custom-server-entrypoint > /usr/local/bin/docker-php-entrypoint

WORKDIR /data
EXPOSE 80