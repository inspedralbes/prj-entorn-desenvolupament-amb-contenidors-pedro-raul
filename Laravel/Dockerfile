# Usa una imagen base con Apache y PHP
FROM php:8.2-apache

# Instala las extensiones de MySQLi
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

ENV COMPOSER_ALLOW_SUPERUSER 1

# Instala las extensiones y dependencias necesarias
RUN apt-get update && \
    apt-get install -y \
        libzip-dev \
        unzip \
        && docker-php-ext-install zip pdo_mysql

# Configura el servidor Apache
RUN a2enmod rewrite

RUN chown -R 777 ./storage


# Instala Composer (el administrador de dependencias de PHP)
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer