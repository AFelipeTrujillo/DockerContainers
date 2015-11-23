## Docker for Symfony2 Projects

### Features
* PHP 5.5
* Mbstring extension
* Intls extension
* SQlite 3 for Development Environment
 
### How to run
```
docker pull afelipetrujillo/php-symfony
sudo docker run -it -p 9999:9999 -v /symfony/project/path:/usr/src/myapp afelipetrujillo/php-symfony
```
Replace **/symfony/project/path** to your local folder where is symfony root path project.

### Dockerfile

```
FROM debian
FROM php:5.5

WORKDIR /usr/src/myapp

COPY ./php.ini /usr/local/etc/php/

RUN apt-get update && apt-get install -y zlib1g-dev libicu-dev g++
RUN docker-php-ext-install mbstring
RUN docker-php-ext-configure intl && docker-php-ext-configure intl && docker-php-ext-install intl

CMD ["php","app/console","server:run","0.0.0.0:9999"]

```
