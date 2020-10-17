FROM docker.io/bitnami/php-fpm:7.4-debian-10

RUN apt-get update
RUN apt-get install nano

ARG SOURCE_ROOT_PATH=./
ENV SOURCE_ROOT_PATH ${SOURCE_ROOT_PATH}

ARG PUID=1000
ENV PUID ${PUID}

ARG PGID=1000
ENV PGID ${PGID}

RUN chmod -R 0777 /opt/bitnami

RUN groupadd -g 1001 bitnami
RUN useradd -u 1001 -g bitnami -m bitnami
RUN usermod -p "*" bitnami -s /bin/bash

RUN groupadd -g ${PGID} developer
RUN useradd -u ${PUID} -g developer -m developer -G bitnami
RUN usermod -p "*" developer -s /bin/bash

RUN chown ${PUID}:${PGID} /app

USER ${PUID}:${PGID}

RUN curl -s https://octobercms.com/api/installer | php

EXPOSE 9000
