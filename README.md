# 📝 TaskList API

Uma API RESTful simples para cadastro de usuários, desenvolvida com Node.js, Express e Sequelize utilizando PostgreSQL como banco de dados.

---

## 🚀 Tecnologias Utilizadas

- **Node.js**  
- **Express**
- **Sequelize ORM**
- **PostgreSQL**
- **ESModules (import/export)**
- **Migrations (sequelize-cli)**

---

## 📁 Estrutura do Projeto

```
tasklist/
├── app/
│   └── models/
│       └── User.js
├── config/
│   └── config.json
├── database/
│   └── migrations/
│       └── 20250325015427-create-users.js
├── src/
│   └── index.js
├── routes.js
├── app.js
├── server.js
```

---

## ⚙️ Requisitos para Rodar o Projeto

Antes de iniciar, você precisará ter instalado:

- **Node.js** (v14 ou superior)
- **PostgreSQL** (e criar uma base chamada `tasklist`)
- **npm** ou **yarn**
- **Sequelize CLI** (caso ainda não tenha)

```bash
npm install -g sequelize-cli
```

---

## 🛠️ Instalação e Execução

### 1. Clone o repositório

```bash
git clone https://github.com/seuusuario/tasklist.git
cd tasklist
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure o banco de dados

Verifique `config/config.json` e ajuste se necessário:

```json
{
  "username": "postgres",
  "password": "admin",
  "database": "tasklist",
  "host": "localhost",
  "dialect": "postgres"
}
```

### 4. Crie o banco no PostgreSQL

```sql
CREATE DATABASE tasklist;
```

### 5. Rode as migrations

```bash
npx sequelize-cli db:migrate
```

### 6. Inicie o servidor

```bash
npm run dev
# ou
node server.js
```

Servidor estará disponível em: [http://localhost:3333](http://localhost:3333)

---

## 📌 Rotas de Teste

### Criar Usuário (Rota de exemplo)
`GET /teste`

Cria um usuário fictício para testes. Está definido em `routes.js`:
```js
{
  name: 'Bryan',
  email: 'bryan@bryan.com',
  password_hash: '123123'
}
```

---

## 🔐 Observação sobre Segurança

Atualmente a API armazena `password_hash` diretamente. É recomendado utilizar o pacote **bcryptjs** para hash seguro de senhas:

```bash
npm install bcryptjs
```

---

## 📬 Contato

Desenvolvido por **Bryan Botelho**  
[LinkedIn](https://www.linkedin.com/in/bryan-botelho/)  
[GitHub](https://github.com/bryanbotelho)

---
