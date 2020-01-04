# laravel_env
Docker compose do ambiente do curso de Laravel Impacta

```yml
version: "3"
services:
  web:
    container_name: nginx_php
    image: webdevops/php-nginx-dev:7.4
    working_dir: /app
    ports:
      - "80:80"
    volumes:
      - .:/app
    environment:
      - WEB_DOCUMENT_ROOT=/app/public
      - PHP_DATE_TIMEZONE=America/Sao_Paulo
  mysql:
    image: mysql:5.7
    ports: 
      - "3306:3306"
    environment:
      - MYSQL_ROOT_PASSWORD=123456
      - MYSQL_DATABASE=getbooked
```
