FROM python:3.8-slim
LABEL MAINTAINER "Yzi <guoyaozhide@gmail.com>"

RUN set -ex \
        && apt-get -y update \
        && apt-get -y install cron \
        && pip3 install greenlet!=0.4.17 \
        && pip3 install subfinder \
        && echo '*/30 * * * * /usr/local/bin/subfinder -c /config/subfinder.json /media > /proc/1/fd/1 2>/proc/1/fd/2' > /etc/cron.d/root \
        && crontab /etc/cron.d/root \
        && rm -rf /var/lib/apt/lists/*

CMD ["cron", "-f"]