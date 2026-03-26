Antes de gerar, uma observação rápida no back:
Nenhuma rota tem try/catch. Se o Prisma lançar um erro, o servidor quebra sem resposta adequada. Não precisa resolver agora, mas anota pra uma próxima versão.
Agora os READMEs e commits:

README — Back (node-express-prisma-crud)
markdown# node-express-prisma-crud

API REST de cadastro de usuários desenvolvida com Node.js, Express e Prisma ORM.

## Tecnologias

- Node.js
- Express
- Prisma ORM
- SQLite
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
   npx prisma migrate dev
```

5. Inicie o servidor

```bash
   node server.js
```

## Requisição de exemplo

```json
{
  "name": "João",
  "age": 23,
  "email": "joao@email.com"
}
```
