FROM wordpress:6.5.3-php8.3-apache
#FROM wordpress:php7.4-fpm

RUN apt-get update && \
    apt-get -y install git

COPY files-to-copy/ /

RUN apt-get -y install libcurl4-openssl-dev
RUN docker-php-ext-install curl
RUN docker-php-ext-enable curl
