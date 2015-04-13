FROM dockerfile/nginx

RUN apt-get update && \
    apt-get -y install nginx apache2-utils

ADD . /tmp/nginx-proxy
WORKDIR /tmp/nginx-proxy

CMD ["bash", "run"]
