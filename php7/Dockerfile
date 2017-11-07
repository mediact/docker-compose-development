FROM srcoder/development-php:php7-fpm
MAINTAINER Jeroen Boersma <jeroen@srcode.nl>

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app

RUN apt-get update && apt-get install -y libmagickwand-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
RUN pecl install imagick && docker-php-ext-enable imagick
RUN echo "xdebug.remote_autostart=1" >> /usr/local/etc/php/conf.d/xdebug.ini

