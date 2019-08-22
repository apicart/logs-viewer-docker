FROM php:7.3-fpm-alpine

RUN apk add --no-cache composer

WORKDIR /var/www

RUN rm -rf *

RUN composer create-project apicart/logs-viewer .

CMD ["php", "-S", "[::]:80", "-t", "public"]

EXPOSE 80
