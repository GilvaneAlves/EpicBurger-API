```markdown
# API EpicBurguer 🍔

API RESTful para gerenciamento completo de pedidos de uma hamburgueria, incluindo **usuários, autenticação, produtos, categorias, pedidos e processamento de pagamentos**, construída com foco em **arquitetura escalável, organização em camadas e simulação de ambiente real de produção**.

---

## 🎯 Problema que o Projeto Resolve

Aplicações de pedidos exigem controle consistente de usuários, catálogo de produtos, categorias e fluxo de pedidos, além de autenticação segura e integração com pagamentos.

A **API EpicBurguer** centraliza essas responsabilidades em uma API bem estruturada, permitindo integração com aplicações frontend e simulando um backend próximo de sistemas reais de delivery.

---

## 🚀 Destaques Técnicos

- **Arquitetura REST em camadas** (controllers, middlewares, models, schemas)
- **Autenticação stateless com JWT**
- **Controle de permissões** (usuário e administrador)
- **Integração com Stripe** para processamento de pagamentos
- **Bancos de dados dual**:
  - PostgreSQL (Sequelize) → dados relacionais
  - MongoDB (Mongoose) → dados flexíveis
- **Validação de dados** com Yup
- **Upload de arquivos** com Multer
- **Estrutura escalável** e pronta para produção

---

## 🧠 Arquitetura e Organização

O projeto segue uma separação clara de responsabilidades para facilitar a manutenção e a escalabilidade:

```
src/
├── app/
│   ├── controllers/      # Lógica de requisições e respostas
│   ├── middlewares/      # Autenticação, autorização, validação
│   ├── models/           # Modelagem de dados (Sequelize e Mongoose)
│   └── schemas/          # Validação de entrada (Yup)
│
├── config/               # Configurações externas (Multer, Stripe)
├── database/             # Conexões e migrations
├── uploads/              # Armazenamento temporário de arquivos
├── routes.js             # Definição de rotas
├── app.js                # Configuração da aplicação
└── server.js             # Ponto de entrada
```

Essa abordagem **facilita manutenção, testes e escalabilidade** do sistema.

---

## 🛠 Tecnologias Utilizadas

| Categoria | Tecnologias 
| **Bancos de Dados** | PostgreSQL (Sequelize), MongoDB (Mongoose) |
| **Validação** | Yup |
| **Pagamentos** | Stripe API |

---

## ✨ Funcionalidades Principais

✅ Cadastro e **autenticação de usuários**  
✅ **Controle de permissões** (admin e usuário comum)  
✅ **CRUD completo** de produtos e categorias  
✅ Criação, listagem e atualização de **pedidos**  
✅ **Upload de imagens** de produtos  
✅ **Validação robusta** de dados de entrada  
✅ **Proteção de rotas** com middleware de autenticação  
✅ **Integração com Stripe** para pagamentos seguros  

---

## 💳 Fluxo de Pagamento (Stripe)

O projeto implementa um fluxo de pagamento seguro utilizando **Stripe Payment Intents**:

1. Frontend solicita criação do pagamento à API
2. API cria um **PaymentIntent** via Stripe
3. Retorna o `client_secret` ao frontend
4. Frontend finaliza o pagamento com **Stripe Elements**
5. API confirma o pagamento e atualiza o pedido

Esse fluxo simula um cenário real de checkout em aplicações modernas.

---

## ▶️ Como Executar o Projeto

### Pré-requisitos

- **Node.js** >= 16
- **npm** ou **yarn**
- **PostgreSQL** rodando localmente
- **MongoDB** rodando localmente (ou Atlas cloud)
- Conta **Stripe** com API keys

### Passos de Instalação

```bash
# Clonar repositório
git clone https://github.com/GilvaneAlves/EpicBurger-API.git

# Entrar no diretório
cd EpicBurger-API

# Instalar dependências
npm install
```

### Configurar Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
# Banco de Dados (PostgreSQL)
DB_HOST=localhost
DB_USER=seu_usuario
DB_PASS=sua_senha
DB_NAME=epicburguer_db
DB_PORT=5432

# Banco de Dados (MongoDB)
MONGO_URI=mongodb://localhost:27017/epicburguer
# ou para Atlas:
# MONGO_URI=mongodb+srv://usuario:senha@cluster.mongodb.net/epicburguer

# Autenticação
JWT_SECRET=sua_chave_jwt_super_secreta

# Stripe
STRIPE_SECRET_KEY=sk_test_sua_chave_stripe
STRIPE_PUBLISHABLE_KEY=pk_test_sua_chave_publica

# Servidor
PORT=3000
NODE_ENV=development
```

### Executar Migrations

```bash
# Criar tabelas no PostgreSQL
npx sequelize-cli db:migrate

# Opcional: Popular banco com dados iniciais
npx sequelize-cli db:seed:all
```

### Iniciar Servidor

```bash
# Modo desenvolvimento (com hot reload)
npm run dev

# Modo produção
npm run build
npm start
```

A API estará disponível em **`http://localhost:3000`**

---

## 🔄 Fluxo de Desenvolvimento

1. **Clone e instale** as dependências do projeto.
2. **Configure o `.env`** com suas credenciais de banco de dados e Stripe.
3. **Execute as migrations** para criar o schema do PostgreSQL.
4. **Inicie o servidor** com `npm run dev`.
5. **Teste os endpoints** via Postman, Insomnia ou ferramenta similar.
6. **Integre com o frontend** (EpicBurger Interface) para uma experiência completa.

---

## 📚 Rotas Principais (Exemplos)

| `POST` | `/sessions` | Realizar login e obter JWT |
| `POST` | `/products` | Criar um novo produto (acesso admin) |
| `POST` | `/orders` | Criar um novo pedido |

---

## 🧪 Testes (Próximos Passos)

Para executar testes automatizados (quando implementados):

```bash
# Rodar testes
npm test

# Com cobertura de código
npm run test:coverage
```

---

## 🛣 Melhorias Futuras

- 🧪 Testes automatizados (Jest / Supertest)
- 📖 Documentação com **Swagger/OpenAPI**
- 📊 **Paginação e filtros avançados** para listagens
- 📋 **Logs estruturados** para observabilidade
- 🐳 **Containerização com Docker**
- 🔄 **CI/CD** (GitHub Actions) para deploy contínuo
- 🔐 **Rate limiting** e proteção DDoS
- 📧 **Notificações por email** (pedidos, confirmações)

---

## 📄 Licença

Este projeto está licenciado sob a **MIT License** – consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 👨‍💻 Autor

**Gilvane Alves Dias**  
Desenvolvedor Full Stack

🔗 **GitHub:** [https://github.com/GilvaneAlves](https://github.com/GilvaneAlves)

---
```
