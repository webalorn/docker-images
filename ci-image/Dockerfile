FROM ubuntu

MAINTAINER webalorn <webalorn@gmail.com>

RUN apt-get update && \
	apt-get install -y php curl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

CMD ["/bin/sh"]

ENTRYPOINT ["/bin/sh", "-c"]