<h1 align="center">Projeto Web Service</h1>

Bem-vindo ao Projeto Web Service! Este projeto é uma aplicação Laravel para gerenciamento de usuários com informações pessoais e endereços associados.

Configuração do Ambiente

### Certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

PHP 7.4
Composer
MySQL ou SQLite

### Configuração do SQLite

Se estiver utilizando SQLite como banco de dados, certifique-se de descomentar a extensão `sqlite` no seu arquivo `php.ini`. Abra o arquivo `php.ini` e remova o ponto e vírgula (;) da frente da linha que contém;

Ps. O .env.example é config em sqlite, pra utilizar o projeto basta copiar para .env as config, e fazer o passo acima no php.ini


### Configuração do Projeto

1 - Clone este repositório para o seu ambiente local:


2 - Instale as dependências do Laravel:
`composer install`

3 - Copie o arquivo de ambiente .env:
`cp .env.example .env`
ps - Caso não for usar o sqlite, configure o arquivo .env com suas configurações de banco de dados e outras configurações necessárias.

4 - Gere a chave de aplicativo:
`php artisan key:generate` 

5 - Execute as migrações do banco de dados:
`php artisan migrate`

6 - Inicie o servidor de desenvolvimento:
`php artisan serve`

A aplicação estará disponível em http://localhost:8000.

### Endpoints da API
A API oferece os seguintes endpoints:

Listar todos os usuários:
GET /api/user

Cadastrar um novo usuário:
POST /api/user

Body da requisição:
json
{
  "name": "Nome do Usuário",
  "email": "usuario@example.com",
  "password": "senha",
  "phone": "123456789",
  "cpf": "12345678901",
  "address": "Rua Principal",
  "number": "123",
  "complement": "Apto 4",
  "neighborhood": "Bairro",
  "zipcode": "12345-678"
}

Obter informações de um usuário específico:
GET /api/user/{id}

Atualizar informações de um usuário:
PUT /api/user/{id}

Body da requisição:
json
{
  "name": "Novo Nome",
  "phone": "987654321"
}


Excluir um usuário:
DELETE /api/user/{id}

### Testes Unitários

Execute os testes unitários com o seguinte comando:
`vendor/bin/phpunit`

<div align="center">
    <p><i>Developed by <a href="URL_LINKEDIN">NOME</i></p>
</div>
