FROM ubuntu

MAINTAINER webalorn <webalorn@gmail.com>

RUN apt-get update && \
	apt-get install -y php curl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN apt-get install -y docker docker-compose

CMD ["/bin/sh"]

ENTRYPOINT ["/bin/sh", "-c"]