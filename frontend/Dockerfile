FROM php:7.2-apache
# Versao Dockerhub

# Enable mysqli to connect to databse
RUN docker-php-ext-install mysqli

# Document Root
#Diretório padrao (Como seria o htdocs no xampp)
WORKDIR /var/www/html/

COPY . /var/www/html/