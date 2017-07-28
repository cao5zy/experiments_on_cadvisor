FROM ubuntu:16.04
RUN apt-get update; apt-get install wget -y;
RUN cd /; \
    mkdir prometheus; \
    cd prometheus; \
    wget https://github.com/prometheus/prometheus/releases/download/v1.7.1/prometheus-1.7.1.linux-amd64.tar.gz; \
    tar xvfz prometheus-1.7.1.linux-amd64.tar.gz; \
    cd prometheus-1.7.1.linux-amd64

WORKDIR /prometheus/prometheus-1.7.1.linux-amd64
ADD prometheus.yml prometheus.yml

CMD ["-config.file=prometheus"]
ENTRYPOINT ./prometheus
