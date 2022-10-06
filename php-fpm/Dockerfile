FROM php:8.1-fpm-alpine

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install bcmath
RUN mkdir -p /var/www/html
 
COPY ./ukb-app-api /var/www/html