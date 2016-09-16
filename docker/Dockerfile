FROM php:7.0-fpm

RUN apt-get update \
    && apt-get install -y --no-install-recommends  libpq-dev libpq5 git \
    && docker-php-ext-install pdo_pgsql pdo_mysql \
    && apt-get purge -y --auto-remove libpq-dev \
    && rm -rf /var/lib/apt/lists/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/html/site/