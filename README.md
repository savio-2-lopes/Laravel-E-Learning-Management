# E-Learning

### Rodando o servidor
sudo docker compose up --build

## Entre no terminal
sudo docker exec -it php-apache bash

## Instale as depedências
composer update

### Ajustando erros de permissão
chmod -R 777 /var/www/php/