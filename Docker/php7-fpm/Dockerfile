FROM php:7-fpm

RUN apt-get update
RUN apt-get install -y wget software-properties-common python-software-properties
RUN echo "deb http://packages.dotdeb.org jessie all" >> /etc/apt/sources.list
RUN wget https://www.dotdeb.org/dotdeb.gpg
RUN apt-key add dotdeb.gpg
RUN apt-get update && apt-get install -y php7.0-common \
    php7.0-cli \
    php7.0-curl \
    php7.0-gd \
    php7.0-imagick \
    php7.0-intl \
    php7.0-json \
    php7.0-mcrypt \
    php7.0-mysql \
    php7.0-opcache

RUN docker-php-ext-install mysqli pdo_mysql

ADD php.ini /usr/local/etc/php/
ADD example.pool.conf /etc/php5/fpm/pool.d/

RUN usermod -u 1000 www-data

CMD ["php-fpm", "-F"]
EXPOSE 9000
