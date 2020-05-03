FROM php:7.3-fpm

RUN apt-get update -y
RUN apt-get install -y git libzip-dev

RUN docker-php-ext-install pdo_mysql mysqli zip

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php
RUN php -r "unlink('composer-setup.php');"
RUN mv composer.phar /usr/local/bin/composer
RUN composer self-update

RUN composer global require "laravel/installer=~1.1"
RUN export PATH="$PATH:~/.composer/vendor/bin"
