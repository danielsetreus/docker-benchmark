FROM phpdockerio/php:8.1-fpm

RUN sed -Ei 's/^# deb-src /deb-src /' /etc/apt/sources.list
RUN apt-get update \
 && apt-get install -y build-essential autoconf libtool pkg-config git-core wget php-imagick wget php8.1-dev \
 && apt-get build-dep -y imagemagick libmagickcore-dev libde265 libheif

RUN apt-get update \
    && apt-get -y --no-install-recommends install ssh-client git php8.1-mysql php8.1-soap php8.1-redis php8.1-bcmath php8.1-gd php8.1-imagick php8.1-xdebug php8.1-imagick php8.1-intl php8.1-curl php8.1-xml php8.1-mbstring php8.1-zip netcat libfcgi-bin unzip mysql-client \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

WORKDIR /home/app  