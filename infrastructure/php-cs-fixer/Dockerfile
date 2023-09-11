FROM php:8.2-fpm-alpine

RUN curl -L https://github.com/PHP-CS-Fixer/PHP-CS-Fixer/releases/download/v3.26.1/php-cs-fixer.phar -o php-cs-fixer && \
    chmod a+x php-cs-fixer && \
    mv php-cs-fixer /usr/local/bin/php-cs-fixer