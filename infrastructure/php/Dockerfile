FROM php:7.4-fpm-alpine

ARG PSYSH_DIR=/usr/local/share/psysh
ARG PHP_MANUAL_URL=http://psysh.org/manual/ja/php_manual.sqlite

WORKDIR /var/www/html

ARG TZ=Asia/Tokyo

RUN set -eux && \
    apk update && \
    apk add --update --no-cache --virtual=.build-dependencies \
        autoconf \
        gcc \
        g++ \
        make \
        tzdata && \
    apk add --update --no-cache \
        oniguruma-dev \
        icu-dev \
        freetype \
        libpng \
        libjpeg-turbo \
        freetype-dev \
        libpng-dev \
        libjpeg-turbo-dev \
        libzip-dev && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    echo ${TZ} > /etc/timezone && \
    pecl install xdebug && \
    apk del .build-dependencies && \
    docker-php-ext-install intl pdo_mysql mbstring zip bcmath && \
    docker-php-ext-configure gd --with-freetype=/usr/include/ --with-jpeg=/usr/include/ && \
    docker-php-ext-install -j$(nproc) gd && \
    docker-php-ext-enable xdebug && \
    mkdir $PSYSH_DIR && wget $PHP_MANUAL_URL -P $PSYSH_DIR

COPY php.ini /usr/local/etc/php