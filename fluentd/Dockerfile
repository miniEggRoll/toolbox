FROM kiyoto/fluentd:0.10.56-2.1.1

RUN mkdir /etc/fluent
RUN apt-get update &&\
    apt-get install --yes make libcurl4-gnutls-dev
RUN ["/usr/local/bin/gem", "install", "fluent-plugin-record-reformer", "--no-rdoc", "--no-ri"]
RUN ["/usr/local/bin/gem", "install", "fluent-plugin-elasticsearch", "--no-rdoc", "--no-ri"]
ADD run /usr/local/bin/run

CMD ["/bin/bash", "/usr/local/bin/run"]
