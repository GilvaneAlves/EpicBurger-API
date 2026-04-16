# API EpicBurguer 🍔

API RESTful desenvolvida para gerenciamento completo de um sistema de pedidos de hamburgueria, contemplando usuários, autenticação, produtos, categorias, pedidos e integração com pagamentos, com foco em boas práticas de backend e arquitetura escalável.

---

## 🎯 Problema que o Projeto Resolve
Sistemas de pedidos exigem controle de usuários, produtos, categorias e fluxo de pedidos, além de autenticação segura.  
Esta API centraliza essas responsabilidades em uma arquitetura organizada e escalável.

---

## 🚀 Destaques Técnicos
- Arquitetura REST em camadas
- Autenticação com JWT
- PostgreSQL + MongoDB
- Integração com Stripe (pagamentos)
- Validação com Yup
- Upload com Multer

---

## 🛠 Tecnologias
Node.js, Express, Sequelize, PostgreSQL, MongoDB, JWT, Multer, Yup, Bcrypt, Stripe

---

## ✨ Funcionalidades
- Autenticação de usuários
- Controle de permissões
- CRUD produtos e categorias
- Pedidos
- Upload de imagens
- Integração com pagamento

---

## 💳 Fluxo de Pagamento
1. Frontend solicita pagamento
2. Backend cria PaymentIntent
3. Retorna client_secret
4. Frontend finaliza pagamento

---

## ▶️ Como rodar

git clone https://github.com/GilvaneAlves/DevBurguerApi.git  
npm install  
npm run dev  

---

## 📁 Estrutura

src/
 ├── controllers  
 ├── middlewares  
 ├── models  
 ├── schemas  
 ├── config  
 ├── database  
 ├── routes.js  
 ├── app.js  
 └── server.js  

---

## 🛣 Melhorias futuras
- Testes
- Swagger
- CI/CD
- Docker

---

## 👨‍💻 Autor
Gilvane Alves Dias
