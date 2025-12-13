# API DevBurguer 🍔

API RESTful desenvolvida para gerenciar um sistema de pedidos de hamburgueria, contemplando **usuários, autenticação, produtos, categorias e pedidos**, com foco em boas práticas de backend e arquitetura escalável.

Projeto desenvolvido com **Node.js**, utilizando **Express**, **Sequelize**, **PostgreSQL** e **MongoDB**, seguindo padrões comuns de aplicações profissionais.

---

## 🎯 Problema que o Projeto Resolve

Sistemas de pedidos para restaurantes exigem controle de usuários, produtos, categorias e pedidos, além de autenticação segura e organização de dados.  
A **API DevBurguer** centraliza essas responsabilidades em uma API bem estruturada, facilitando a integração com aplicações frontend (web ou mobile) e garantindo consistência nos dados.

---

## 👥 Público-Alvo

- Desenvolvedores frontend que precisam consumir uma API de pedidos
- Projetos de restaurantes, lanchonetes ou delivery
- Avaliadores técnicos e recrutadores analisando arquitetura backend

---

## 🧠 Nível Técnico

**Intermediário**

O projeto demonstra domínio de:
- Arquitetura REST
- Autenticação com JWT
- Modelagem de dados relacional e não relacional
- Organização em camadas (controllers, models, middlewares)

---

## 🛠 Tecnologias Utilizadas

- **Node.js**
- **Express**
- **JavaScript (ES Modules)**
- **PostgreSQL**
- **MongoDB**
- **Sequelize ORM**
- **JWT (JSON Web Token)**
- **Multer** (upload de arquivos)
- **Yup** (validação de dados)
- **Bcrypt** (hash de senhas)
- **ESLint / Biome** (padronização de código)

---

## ✨ Funcionalidades

- Cadastro e autenticação de usuários
- Controle de permissões (admin)
- CRUD de produtos
- CRUD de categorias
- Criação e listagem de pedidos
- Upload de imagens de produtos
- Validação de dados de entrada
- Proteção de rotas com middleware de autenticação

---

## ▶️ Como Executar o Projeto Localmente

### 1. Clonar o repositório
```bash
git clone https://github.com/GilvaneAlves/DevBurguerApi.git
```

### 2. Instalar as dependências
```bash
npm install
```

### 3. Configurar o banco de dados
- Configure o arquivo de conexão em:
```
src/config/database.cjs
```

- Crie o banco no PostgreSQL
- Execute as migrations:
```bash
npx sequelize-cli db:migrate
```

### 4. Executar a aplicação
```bash
npm run dev
```

A API estará disponível em:
```
http://localhost:3000
```

---

## 📁 Estrutura de Pastas (Resumo)

```
src/
├── app/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   └── schemas/
├── config/
├── database/
│   └── migrations/
├── routes.js
├── app.js
└── server.js
```

---

## 🛣 Possíveis Melhorias Futuras

- Testes automatizados (Jest / Supertest)
- Documentação com Swagger
- Paginação e filtros avançados
- Logs estruturados
- Deploy com Docker

---

## 📄 Licença

Sugestão de licença **MIT**, adequada para projetos open source e portfólio profissional.

---

## 👨‍💻 Autor

**Gilvane Alves Dias**  
Desenvolvedor Full Stack  
GitHub: https://github.com/GilvaneAlves
