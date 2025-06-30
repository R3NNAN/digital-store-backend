# Digital Store Backend 🛒

API backend em Node.js/Express para gerenciamento de produtos e carrinhos de compras, persistindo dados em arquivos JSON.

## 🧩 Sumário

- [Funcionalidades](#funcionalidades)  
- [Instalação](#instalação)  
- [Uso](#uso)  
  - [Endpoints para produtos](#endpoints-para-produtos)  
  - [Endpoints para carrinhos](#endpoints-para-carrinhos)  
- [Coleções Postman](#coleções-postman)  
- [Tecnologias](#tecnologias)  
- [Ambiente e Deploy](#ambiente-e-deploy)  
- [Testes](#testes)  
- [Contribuição](#contribuição)  

---

## Funcionalidades

- ✅ Operações CRUD completas para **Produtos**  
- 🛒 Criação e atualização de **carrinhos de compras**  
- 💾 Armazenamento de dados em **arquivos JSON** sem banco de dados  
- 🚀 Estrutura pronta para futuras implementações como autenticação de usuário

---

## Instalação

```bash
git clone https://github.com/R3NNAN/digital-store-backend.git
cd digital-store-backend
npm install
npm start
````

> O servidor iniciará por padrão em `http://localhost:3000/` (ou porta definida no `.env`).

---

## Uso

### Endpoints para Produtos

| Método | Endpoint             | Descrição                        |
| ------ | -------------------- | -------------------------------- |
| GET    | `/api/products/`     | Lista todos os produtos          |
| GET    | `/api/products/:pid` | Exibe dados de um produto por ID |
| POST   | `/api/products/`     | Adiciona um novo produto         |
| PUT    | `/api/products/:pid` | Atualiza produto por ID          |
| DELETE | `/api/products/:pid` | Remove produto por ID            |

### Endpoints para Carrinhos

| Método | Endpoint                        | Descrição                                  |
| ------ | ------------------------------- | ------------------------------------------ |
| POST   | `/api/carts/`                   | Cria um novo carrinho                      |
| GET    | `/api/carts/:cid`               | Retorna um carrinho com base no ID         |
| POST   | `/api/carts/:cid/products/:pid` | Adiciona um produto ao carrinho específico |

---

## Coleções Postman

Importe os seguintes arquivos no Postman para testar os endpoints:

* `PrimeraEntrega-Products.postman_collection.json`
* `PrimeraEntrega-Carts.postman_collection.json`

> Certifique-se de que o servidor esteja rodando antes de enviar requisições via Postman.

---

## Tecnologias

* **Node.js** com **Express.js** – servidor backend
* **ESLint** – padrão de código
* **Armazenamento em arquivos JSON** (sem banco de dados)
* **Postman** para testes de endpoints REST

---

## Ambiente e Deploy

### Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
PORT=3000
```

> Você pode mudar a porta conforme sua necessidade.

### Deploy Local

```bash
# Instale as dependências
npm install

# Inicie o servidor
npm start
```

---

## Testes

Atualmente os testes são feitos manualmente através do Postman. Recomenda-se:

* Verificar todos os endpoints com dados válidos e inválidos
* Validar estrutura dos arquivos `products.json` e `carts.json`
* Usar ferramentas como `nodemon` durante o desenvolvimento

> Para testes automatizados (futuros), considere bibliotecas como `Jest` ou `Supertest`.

---

## Contribuição

Contribuições são bem-vindas! Para colaborar:

1. Faça um fork do repositório
2. Crie uma branch (`git checkout -b feature/nome-da-feature`)
3. Faça seus commits (`git commit -m "sua feature"`)
4. Envie um Pull Request

---
