## API em produção
🔗 `https://node-express-prisma-crud.onrender.com`

API REST de cadastro de usuários desenvolvida com Node.js, Express e Prisma ORM.

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

1. Clone o repositório
2. Instale as dependências

```bash
   npm install
```

3. Configure o `.env` com base no `.env.example`
4. Rode as migrations

```bash
   npx prisma db push
```

5. Inicie o servidor

```bash
   npm run start
```

## Requisição de exemplo

```json
{
  "name": "João",
  "age": 23,
  "email": "joao@email.com"
}
```
