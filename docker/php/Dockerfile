FROM php:7.2-fpm-alpine

RUN apk update

# DOC : https://hub.docker.com/_/php

# needed for composer
RUN apk add --no-cache libzip-dev
RUN apk add --no-cache wget

RUN apk add --no-cache git
RUN apk add --no-cache nano

# mysql
RUN docker-php-ext-install pdo
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/app