FROM debian
FROM php:5.5

WORKDIR /usr/src/myapp

COPY ./php.ini /usr/local/etc/php/

RUN apt-get update && apt-get install -y zlib1g-dev libicu-dev g++
RUN docker-php-ext-install mbstring
RUN docker-php-ext-configure intl && docker-php-ext-configure intl && docker-php-ext-install intl

CMD ["php","app/console","server:run","0.0.0.0:9999"]


