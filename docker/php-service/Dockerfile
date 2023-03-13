FROM php:8.2.3-fpm

ARG user
ARG uid

RUN apt-get -y update

RUN apt-get -y install zip unzip wget 

RUN docker-php-ext-install bcmath pdo_mysql \

COPY --from=composer:2.5.4 /usr/bin/composer /usr/bin/composer

RUN useradd -G www-data,root -u $uid -d /home/$user $user

RUN mkdir -p /home/$user/.composer && \
    chown -R $user:$user /home/$user

USER $user