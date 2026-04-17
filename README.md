# API EpicBurguer 🍔

API RESTful para gerenciamento completo de pedidos de uma hamburgueria, incluindo **usuários, autenticação, produtos, categorias, pedidos e processamento de pagamentos**, construída com foco em **arquitetura escalável, organização em camadas e simulação de ambiente real de produção**.

---

## 🎯 Problema que o Projeto Resolve

Aplicações de pedidos exigem controle consistente de usuários, catálogo de produtos, categorias e fluxo de pedidos, além de autenticação segura e integração com pagamentos.

A **API DevBurguer** centraliza essas responsabilidades em uma API bem estruturada, permitindo integração com aplicações frontend e simulando um backend próximo de sistemas reais de delivery.

---

## 🚀 Destaques Técnicos

- Arquitetura REST organizada em camadas (**controllers, middlewares, models e schemas**)
- Autenticação stateless com **JWT**
- Controle de permissões (usuário e administrador)
- Integração com **Stripe** para processamento de pagamentos
- Uso combinado de:
  - **PostgreSQL (Sequelize)** → dados relacionais
  - **MongoDB (Mongoose)** → dados flexíveis
- Validação de dados com **Yup**
- Upload de arquivos com **Multer**
- Estrutura preparada para escalabilidade e manutenção

---

## 🧠 Arquitetura e Organização

O projeto segue separação clara de responsabilidades:

- **Controllers** → recebem e tratam requisições
- **Middlewares** → autenticação e autorização
- **Models** → acesso e modelagem de dados
- **Schemas** → validação de entrada
- **Config** → configurações externas (ex: upload)
- **Database** → conexão e migrations

Essa abordagem facilita manutenção, testes e evolução do sistema.

---

## 🛠 Tecnologias Utilizadas

- **Node.js**
- **Express**
- **JavaScript (ES Modules)**
- **PostgreSQL + Sequelize**
- **MongoDB + Mongoose**
- **JWT (JSON Web Token)**
- **Multer**
- **Yup**
- **Bcrypt**
- **Stripe API**
- **ESLint / Biome**

---

## ✨ Funcionalidades

- Cadastro e autenticação de usuários
- Controle de permissões (admin)
- CRUD completo de produtos e categorias
- Criação, listagem e atualização de pedidos
- Upload de imagens de produtos
- Validação de dados de entrada
- Proteção de rotas com middleware
- Integração com pagamentos via Stripe

---

## 💳 Fluxo de Pagamento (Stripe)

O projeto implementa um fluxo de pagamento utilizando **Stripe Payment Intents**:

1. O frontend solicita a criação do pagamento
2. O backend cria um **PaymentIntent** via Stripe
3. Retorna o `client_secret` ao frontend
4. O frontend finaliza o pagamento com Stripe Elements

Esse fluxo simula um cenário real de checkout em aplicações modernas.

---

## ▶️ Como Executar o Projeto

### 1. Clonar o repositório
```bash
git clone https://github.com/GilvaneAlves/EpicBurger-API.git
```

### 2. Instalar dependências
```bash
npm install
```

### 3. Configurar variáveis de ambiente

Crie um arquivo `.env`:

```env
DB_HOST=
DB_USER=
DB_PASS=
DB_NAME=
JWT_SECRET=
STRIPE_SECRET_KEY=
```

### 4. Rodar migrations
```bash
npx sequelize-cli db:migrate
```

### 5. Iniciar servidor
```bash
npm run dev
```

API disponível em:
```
http://localhost:3000
```

---

## 📁 Estrutura de Pastas

```
src/
├── app/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   ├── schemas/
│
├── config/
├── database/
├── uploads/
├── routes.js
├── app.js
└── server.js
```

---

## 🛣 Melhorias Futuras

- Testes automatizados (Jest / Supertest)
- Documentação com Swagger
- Paginação e filtros avançados
- Logs estruturados (observabilidade)
- Containerização com Docker
- CI/CD

---

## 📄 Licença

MIT

---

## 👨‍💻 Autor

**Gilvane Alves Dias**  
Desenvolvedor Full Stack  
GitHub: https://github.com/GilvaneAlves
