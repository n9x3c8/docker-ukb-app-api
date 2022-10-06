FROM composer:latest
FROM php:8.1

#install composer 
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update && \
  apt-get install -y software-properties-common && \
  rm -rf /var/lib/apt/lists/*
 
#install tools
RUN apt-get update && apt-get install -y git curl vim nano net-tools pkg-config iputils-ping apt-utils zip unzip
 
RUN docker-php-ext-install bcmath pdo_mysql

RUN mkdir -p /var/www/html
COPY ./ukb-app-api /var/www/html