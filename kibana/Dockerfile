FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && \
    apt-get install -y nginx-full wget vim curl
RUN wget https://download.elasticsearch.org/kibana/kibana/kibana-3.1.0.tar.gz -O /tmp/kibana.tar.gz && \
    tar zxf /tmp/kibana.tar.gz && mv kibana-3.1.0/* /usr/share/nginx/html
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
ADD run.sh /usr/local/bin/run
ADD server.conf /etc/nginx/conf.d/kibana.conf
EXPOSE 80
CMD ["/bin/bash", "/usr/local/bin/run"]
