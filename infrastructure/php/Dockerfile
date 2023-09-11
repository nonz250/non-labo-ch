FROM php:8.2-fpm-alpine

ARG TZ=Asia/Tokyo

WORKDIR /var/www/html

RUN set -eux && \
    apk update && \
    apk add --no-cache \
        oniguruma-dev \
        icu-dev \
        freetype \
        linux-headers \
        libpng \
        libjpeg-turbo \
        freetype-dev \
        libpng-dev \
        libjpeg-turbo-dev \
        libzip-dev && \
    apk add --no-cache --virtual=.build-dependencies \
        autoconf \
        gcc \
        g++ \
        make \
        tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    echo ${TZ} > /etc/timezone && \
    pecl install xdebug && \
    apk del .build-dependencies && \
    docker-php-ext-install -j$(nproc) intl mbstring pdo_mysql gd zip bcmath && \
    docker-php-ext-configure gd --with-freetype=/usr/include/ --with-jpeg=/usr/include/ && \
    docker-php-ext-enable xdebug

COPY php.ini /usr/local/etc/php
