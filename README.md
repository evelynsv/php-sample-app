# Sistemas para internet - Devops

#Executando uma aplicação baseada em php e mysql em containers.

Clone a aplicação executando : git clone https://github.com/

Os arquivos dockerfile ja foram configurados, você os encontrará nas pastas "Frontend" e "Backend".

Execute o Docker Quickstart Terminal e salve o ip que ele retorna na execução.

Entre na pasta da sua aplicação e execute:
docker pull php:7.2-apache
docker pull mysql:5.7

Entre na pasta backend e execute:
docker build . -t backend-mysql:0.1

Execute na pasta frontend:
docker build . -t frontend-php:0.1

Execute:
docker run -d --rm --name backend -e MYSQL_DATABASE=demo -e MYSQL_ALLOW_EMPTY_PASSWORD=yes backend-mysql:0.1

docker run -d --rm --name frontend -p 80:80 --link backend frontend-php:0.1

docker ps

Acesse o endereço de ip que é passado quando você starta o Docker Quickstart Terminal: 192.168.99.100:80


