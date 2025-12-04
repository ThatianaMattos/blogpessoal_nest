📘 Blog Pessoal – CRUD com NestJS

Este repositório contém a implementação da primeira parte do CRUD de Postagens utilizando NestJS, TypeORM e MySQL, conforme solicitado na atividade WEB-JS-2 – Atividade CRUD – Blog Pessoal.

🚀 Tecnologias utilizadas

NestJS

TypeORM

MySQL

TypeScript

Insomnia (para testes da API)

✔️ Funcionalidades implementadas (Parte 01)

Criação da Entity Postagem

Criação do Service PostagemService

Criação do Controller PostagemController

Integração com MySQL via TypeORM

Rota GET /postagens retornando lista vinda do banco de dados

Configuração do AppModule com variáveis de ambiente (arquivo .env)

📂 Estrutura do Projeto (src/)
src/
 └── postagem/
     ├── controllers/
     │    └── postagem.controller.ts
     ├── services/
     │    └── postagem.service.ts
     ├── entities/
     │    └── postagem.entity.ts
     └── postagem.module.ts

 app.module.ts
 main.ts

🗃️ Entity: Postagem

Representa a tabela tb_postagens no banco de dados.

Atributos definidos:

id

titulo

texto

data (gerado automaticamente)

🛠️ Service: PostagemService

Responsável pela lógica de negócio e comunicação com o banco via TypeORM Repository.

🎯 Controller: PostagemController

Endpoints disponíveis:

GET /postagens
Retorna todas as postagens cadastradas.

🧪 Testando a API
Endpoint principal implementado nesta fase:

GET

http://localhost:3000/postagens

Resposta esperada:
[
  {
    "id": 1,
    "titulo": "Postagem 01",
    "texto": "Texto da postagem 01",
    "data": "2025-12-03T20:01:53.000Z"
  }
]

🛠️ Configuração do Banco de Dados

A aplicação utiliza variáveis de ambiente:

DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=SUA_SENHA
DB_NAME=db_blogpessoal


O NestJS carrega essas variáveis automaticamente via ConfigModule.

▶️ Como rodar o projeto

Instale as dependências:

npm install


Inicie a aplicação:

npm run start:dev


Acesse:

http://localhost:3000/postagens

👩‍💻 Autora

Thatiana Mattos – Desenvolvedora Full Stack

GitHub: https://github.com/ThatianaMattos

LinkedIn: https://www.linkedin.com/in/thatiana-mattos/
