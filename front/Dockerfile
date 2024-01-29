# Usa una imagen base con Apache y PHP
FROM php:8.2-apache

# Instala las extensiones de MySQLi
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Expone el puerto 80 para acceder a la aplicación
EXPOSE 80

# Inicia el servidor Apache al iniciar el contenedor
CMD ["apache2-foreground"]