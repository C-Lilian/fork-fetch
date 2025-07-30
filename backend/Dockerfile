# backend/Dockerfile

FROM php:8.2-apache

# Installer les extensions nécessaires
RUN docker-php-ext-install pdo pdo_mysql

# Active le mod_rewrite pour Apache (utile pour les routes Slim)
RUN a2enmod rewrite

# Copier le projet dans le container
COPY . /var/www/html/

# Définir les droits
RUN chown -R www-data:www-data /var/www/html

# Config Apache
COPY apache-config.conf /etc/apache2/sites-enabled/000-default.conf
