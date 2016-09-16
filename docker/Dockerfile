FROM php:7.0-fpm

RUN apt-get update \
    && apt-get install -y --no-install-recommends  libpq-dev libpq5 \
    && docker-php-ext-install pdo_pgsql pdo_mysql \
    && apt-get purge -y --auto-remove libpq-dev \
    && rm -rf /var/lib/apt/lists/*