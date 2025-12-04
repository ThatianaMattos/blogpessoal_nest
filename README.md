# 📝 Blog Pessoal – CRUD com NestJS

Este repositório contém a implementação da primeira parte do CRUD de Postagens utilizando NestJS, TypeORM e MySQL, conforme solicitado na atividade WEB-JS-2 - Atividade CRUD - Blog Pessoal.

🚀 Tecnologias utilizadas

Node.js

NestJS

TypeORM

MySQL

Insomnia para testes da API

TypeScript

📌 Funcionalidades implementadas (Parte 01)

Criação da Entity Postagem

Criação do Service PostagemService

Criação do Controller PostagemController

Integração com MySQL usando TypeORM

Rota GET /postagens funcionando e retornando lista do banco

Configuração do AppModule com TypeORM

📂 Estrutura do Projeto
src/
 ├── postagem/
 │    ├── controllers/
 │    │      └── postagem.controller.ts
 │    ├── services/
 │    │      └── postagem.service.ts
 │    ├── entities/
 │    │      └── postagem.entity.ts
 │    └── postagem.module.ts
 ├── app.module.ts
 ├── main.ts

📄 Entity: Postagem

Representa a tabela tb_postagens no banco de dados.

🔧 Service: PostagemService

Responsável pelas regras de negócio e comunicação com o banco via TypeORM Repository.

🌐 Controller: PostagemController

Expõe os endpoints da API, incluindo:

GET /postagens – Retorna todas as postagens cadastradas

🧪 Testando a API

A rota principal implementada nesta fase é:

GET <http://localhost:3000/postagens>

Resposta esperada:

[
  {
    "id": 1,
    "titulo": "Postagem 01",
    "texto": "Texto da postagem 01",
    "data": "2025-12-03T20:01:53.000Z"
  }
]

🗄 Configuração do Banco de Dados

A aplicação está configurada para conectar ao MySQL via TypeORM:

TypeOrmModule.forRoot({
  type: 'mysql',
  host: 'localhost',
  port: 3306,
  username: 'root',
  password: 'SUA_SENHA',
  database: 'db_blogpessoal',
  synchronize: true,
  autoLoadEntities: true,
})

📎 Como rodar o projeto

Instale as dependências:

npm install

Inicie a aplicação:

npm run start:dev

Acesse:

<http://localhost:3000/postagens>

📬 Autora

Thatiana Mattos
Desenvolvedora Full Stack
GitHub: <https://github.com/ThatianaMattos>

LinkedIn: <https://www.linkedin.com/in/thatiana-mattos/>
