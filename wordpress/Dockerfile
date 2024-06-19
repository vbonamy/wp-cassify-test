FROM wordpress:6.5.3-php8.3-apache
#FROM wordpress:php7.4-fpm

RUN apt-get update && \
    apt-get -y install git

RUN cd /tmp && \
    git clone https://github.com/xdebug/xdebug.git && \
    cd xdebug && \
    git checkout xdebug_3_3 && \
    phpize && \
    ./configure --enable-xdebug && \
    make && \
    make install && \
    rm -rf /tmp/xdebug

COPY files-to-copy/ /

RUN docker-php-ext-enable xdebug

RUN apt-get -y install libcurl4-openssl-dev
RUN docker-php-ext-install curl
RUN docker-php-ext-enable curl
