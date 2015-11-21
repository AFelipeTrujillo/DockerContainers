FROM debian
FROM php:5.5

WORKDIR /usr/src/myapp

COPY ./php.ini /usr/local/etc/php/

CMD ["php","app/console","server:run","0.0.0.0:9999"]


