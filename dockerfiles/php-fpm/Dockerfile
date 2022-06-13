FROM php:8.1-fpm-alpine3.16

COPY ./php.ini /usr/local/etc/php/php.ini

RUN apk add --no-cache libzip-dev libpng-dev zip curl libxml2-dev oniguruma-dev curl-dev bash
#RUN docker-php-ext-configure zip
RUN docker-php-ext-install mbstring pdo_mysql fileinfo
#RUN docker-php-ext-install zip bcmath gd pdo_mysql curl fileinfo openssl mbstring

WORKDIR /var/www

CMD ["php-fpm"]

EXPOSE 9000