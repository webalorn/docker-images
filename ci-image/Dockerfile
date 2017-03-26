FROM ubuntu

MAINTAINER webalorn <webalorn@gmail.com>

RUN apt-get update && \
	apt-get install -y php curl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN apt-get install -y docker python-pip
RUN pip install --upgrade pip && \
    pip install --upgrade docker-compose

RUN rm /bin/sh && echo 'bash $@' > /bin/sh && chmod 777 /bin/sh

CMD ["bash"]

ENTRYPOINT ["bash", "-c"]
