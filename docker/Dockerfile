FROM php:fpm-alpine

RUN set -ex \
  && apk --no-cache add \
    postgresql-dev


RUN docker-php-ext-install pdo pdo_pgsql pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

COPY php.ini /usr/local/etc/php/

WORKDIR /var/www/html/site/
ONBUILD RUN composer update
