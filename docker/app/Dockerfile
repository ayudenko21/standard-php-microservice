FROM gitlab.21vek.by:5050/repos/microservices/search-history/php-fpm-base:8.1.2-fpm-alpine

# for dev environments only
RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

WORKDIR /var/www/html
ADD . .

COPY docker/app/php/dev/php_dev.ini /usr/local/etc/php/conf.d/php.ini
COPY docker/app/php/dev/opcache_dev.ini /usr/local/etc/php/conf.d/opcache.ini

RUN  chmod -R 777 var && \
    chown -R www-data:www-data .
