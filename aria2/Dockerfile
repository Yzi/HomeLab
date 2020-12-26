FROM ubuntu:focal
LABEL MAINTAINER "Yzi <guoyaozhide@gmail.com>"

RUN set -ex \
        && apt-get -y update \
        && apt-get -y install aria2 \
        && rm -rf /var/lib/apt/lists/*
EXPOSE 6800

ENTRYPOINT ["aria2c"]