FROM php:7.2-apache

# Enable mysqli to connect to databse
RUN docker-php-ext-install mysqli

#diretório padrão, onde vai rodar, document root
WORKDIR /var/www/html/

#copiar diretório e jogar na raíz do servidor, workdir
COPY . /var/www/html/