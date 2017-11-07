FROM srcoder/development-php:php5-fpm
MAINTAINER Jeroen Boersma <jeroen@srcode.nl>

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app

RUN echo "xdebug.remote_autostart=1" >> /usr/local/etc/php/conf.d/xdebug.ini

