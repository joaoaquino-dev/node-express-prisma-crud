# API REST de usuários (Node.js, Express e Prisma)

API de cadastro de usuários com operações de criar, listar, atualizar e remover (CRUD), usando Node.js, Express e Prisma ORM com MongoDB.

Projeto de estudo, feito a partir de um curso e ajustado por mim para deploy em produção (scripts de `build` e `start` e porta dinâmica).

🔗 **API em produção:** `https://node-express-prisma-crud.onrender.com`
🖥️ **Interface que consome esta API:** [react-vite-crud](https://github.com/joaoaquino-dev/react-vite-crud)

## Tecnologias

- Node.js
- Express
- Prisma ORM
- MongoDB
- dotenv
- CORS

## Rotas

| Método | Rota       | Descrição               |
| ------ | ---------- | ----------------------- |
| GET    | /users     | Lista todos os usuários |
| POST   | /users     | Cria um novo usuário    |
| PUT    | /users/:id | Atualiza um usuário     |
| DELETE | /users/:id | Remove um usuário       |

## Como rodar

Pré-requisitos: Node.js e uma instância de MongoDB (por exemplo, no MongoDB Atlas).

1. Clone o repositório
2. Instale as dependências

```bash
npm install
```

3. Crie o arquivo `.env` a partir do exemplo e preencha a `DATABASE_URL`

```bash
cp .env.example .env
```

4. Gere o cliente do Prisma e sincronize o schema com o banco

```bash
npx prisma generate
npx prisma db push
```

5. Inicie o servidor

```bash
npm run start
```

O servidor sobe na porta definida em `PORT` (padrão `3000`).

## Requisição de exemplo

```json
{
  "name": "João",
  "age": 23,
  "email": "joao@email.com"
}
```

O e-mail é único no modelo de usuário.

## Limitações e próximos passos

Este projeto é um CRUD básico de estudo. Ainda não tem:

- Validação dos dados recebidos (formato do e-mail, tipo de `age`) nem tratamento de erros com respostas específicas.
- Testes automatizados.
- Restrição de origens no CORS (hoje aceita qualquer origem).
- Autenticação.

Melhorias planejadas: validação de entrada, tratamento de erros, testes e restrição do CORS.

## Como o projeto foi feito

Projeto de estudo, desenvolvido a partir de um curso. A documentação e os ajustes de deploy foram feitos por mim, com apoio de IA para revisão.

## Autor

João Aquino · [LinkedIn](https://www.linkedin.com/in/jo%C3%A3o-aquino-dev) · [GitHub](https://github.com/joaoaquino-dev)
