<h1 align="center">Laravel E-Learning Management</i> </p>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/savio-2-lopes/laravel-e-learning-management.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/savio-2-lopes/laravel-e-learning-management.svg">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/savio-2-lopes/laravel-e-learning-management.svg">
  <a href="https://github.com/savio-2-lopes/laravel-e-learning-management/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/savio-2-lopes/laravel-e-learning-management.svg">
  </a>

  <a href="https://github.com/savio-2-lopes/laravel-e-learning-management/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/savio-2-lopes/laravel-e-learning-management.svg">
  </a>
</p>


## Tópicos
* [Descrição do Projeto](#descrição-do-projeto)
* [Ferramentas e Tecnologias](#ferramentas-e-tecnologias)
* [Como executar o projeto](#como-executar)
* [Autor](#Autor)

<br>

## Descrição do Projeto

E-Learning em desenvolvimento, com o objetivo de se tornar uma plataforma onde as pessoas possam ter acesso, de forma mais organizada, a cursos e materiais de programação gratuitos de diversos autores.

<br>

## Ferramentas e Tecnologias

* [HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
* [CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
* [Bootstrap](https://getbootstrap.com/)
* [Laravel 9.x](https://laravel.com/)
* [MySQL](https://www.mysql.com/)
* [Git](https://git-scm.com/) 
* [Docker](https://www.docker.com/)

<br>

## Como executar

#### Pré-requisitos
Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas: [Docker](https://www.docker.com/).

<br>

### Rodando a aplicação web 

Primeiro clone o repositório: 

```git clone https://github.com/savio-2-lopes/laravel-e-learning-management.git```
ou 
```git clone git@github.com:savio-2-lopes/laravel-e-learning-management.git```

Acesse a pasta do repositório e realize o build do container: 

```cd laravel-e-learning-management```

```docker compose up --build```

Em outro terminal, no mesmo diretório, entre no Docker com este comando

```docker exec -it e-learning bash```

No container, instale as dependência

```composer update```

  >Caso o Git em seu computador esteja configurado para SSH, deve-se [cadastrar um token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) para realizar o update

Na pasta app/ renomeie o arquivo .env.example para .env

Dentro da pasta app/, no .env, atualize as seguintes variáveis para os dados abaixo:

```
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=db-e-learning
DB_USERNAME=root
DB_PASSWORD=root
```

Após isto, volte para dentro do container Docker e rode as migrations para adicionar as tabelas padrões ao banco de dados

```php artisan key:generate```

```php artisan migrate```

```chmod -R 777 /var/www/php/```

Se tudo estiver correto, a aplicação estará rodando em:
```http://localhost:8000```

<br>

## Autor

[Savio Lopes](https://www.linkedin.com/in/savio-lopes/)