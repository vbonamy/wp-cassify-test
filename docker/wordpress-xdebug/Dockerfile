FROM wordpress:6.5.5-php8.2-apache

RUN apt-get update

RUN apt-get -y install libcurl4-openssl-dev
RUN docker-php-ext-install curl
RUN docker-php-ext-enable curl

RUN pecl install "xdebug" 
RUN docker-php-ext-enable xdebug
RUN echo "xdebug.mode=debug" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

RUN chmod a+rw -R /var/www/html

