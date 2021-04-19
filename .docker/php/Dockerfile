FROM php:8.0.3-fpm-buster

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
        && docker-php-ext-configure gd --with-freetype --with-jpeg \
        && docker-php-ext-install -j$(nproc) gd

RUN apt install -y libzip-dev libxml2-dev vim

RUN docker-php-ext-install pdo_mysql zip soap xml bcmath
