FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
        libonig-dev \
        libzip-dev \
        zip \
  && docker-php-ext-install zip \
  && docker-php-ext-install pdo pdo_mysql mysqli

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www

CMD ["php-fpm"]
