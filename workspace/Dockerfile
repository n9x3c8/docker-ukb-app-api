FROM composer:2.0
FROM php:8.0

#install composer 
COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

RUN apt-get update && \
  apt-get install -y software-properties-common && \
  rm -rf /var/lib/apt/lists/*
 
#install tools
RUN apt-get update && apt-get install -y git curl vim nano net-tools pkg-config iputils-ping apt-utils zip unzip
 
RUN docker-php-ext-install bcmath pdo_mysql

RUN mkdir -p /var/www/html
COPY ./ukb-app-api /var/www/html