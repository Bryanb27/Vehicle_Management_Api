# API de Gerenciamento de Veículos - Desafio Técnico

API REST desenvolvida com Node.js, TypeScript e Express para gerenciamento de veículos, motoristas e registros de utilização de veículos.

## Funcionalidades

### Veículos

* Criar um veículo
* Atualizar um veículo
* Excluir um veículo
* Buscar veículo por ID
* Listar veículos
* Filtrar veículos por cor
* Filtrar veículos por marca

### Motoristas

* Criar um motorista
* Atualizar um motorista
* Excluir um motorista
* Buscar motorista por ID
* Listar motoristas
* Filtrar motoristas por nome

### Utilização de Veículos

* Iniciar utilização de um veículo
* Finalizar utilização de um veículo
* Listar todos os registros de utilização
* Exibir informações do motorista e do veículo nos registros de utilização

## Regras de Negócio

* Um veículo só pode ser utilizado por um motorista por vez.
* Um motorista que já esteja utilizando um veículo não pode utilizar outro veículo simultaneamente.

## Tecnologias

* Node.js
* TypeScript
* Express
* Jest
* Supertest
* UUID

## Demonstração

URL base:

https://vehicle-management-api-seidor.onrender.com

A API está hospedada e pode ser testada utilizando o Postman ou qualquer cliente HTTP.

**Observação:** Este projeto utiliza persistência em memória. Portanto, todos os dados serão reiniciados quando o servidor for reiniciado (por exemplo, durante um novo deploy no Render ou após uma reinicialização por inatividade).

### Exemplos de Endpoints

#### Veículos

* GET /cars
* POST /cars
* GET /cars?color=Black&brand=Toyota

#### Motoristas

* GET /drivers
* POST /drivers
* GET /drivers?name=Bryan

#### Utilização de Veículos

* GET /usages
* POST /usages
* PATCH /usages/:id/finish

## Instalação

Clone o repositório:

```bash
git clone <repository-url>
```

Instale as dependências:

```bash
npm install
```

## Executando a Aplicação

Modo de desenvolvimento:

```bash
npm run dev
```

A API estará disponível em:

```text
http://localhost:3000
```

## Executando os Testes

```bash
npm test
```

## Endpoints da API

### Veículos

| Método | Endpoint  |
| ------ | --------- |
| POST   | /cars     |
| GET    | /cars     |
| GET    | /cars/:id |
| PUT    | /cars/:id |
| DELETE | /cars/:id |

### Motoristas

| Método | Endpoint     |
| ------ | ------------ |
| POST   | /drivers     |
| GET    | /drivers     |
| GET    | /drivers/:id |
| PUT    | /drivers/:id |
| DELETE | /drivers/:id |

### Utilização de Veículos

| Método | Endpoint           |
| ------ | ------------------ |
| POST   | /usages            |
| PATCH  | /usages/:id/finish |
| GET    | /usages            |

## Testes

O projeto inclui:

* Testes unitários dos serviços
* Testes de integração dos endpoints da API
* Testes de validação das regras de negócio

## Estrutura do Projeto

```text
src
├── controllers
├── services
├── repositories
├── routes
├── models
├── middlewares
├── tests
├── container.ts
├── app.ts
└── server.ts
```

### Arquitetura

A aplicação segue uma arquitetura em camadas:

```text
Requisição
   ↓
Rotas
   ↓
Controllers
   ↓
Services
   ↓
Repositories
   ↓
Armazenamento em Memória
```

#### Responsabilidades

* **Rotas**: definição dos endpoints da API.
* **Controllers**: gerenciamento das requisições e respostas HTTP.
* **Services**: implementação das regras de negócio e da lógica da aplicação.
* **Repositories**: gerenciamento da persistência dos dados em memória.
* **Models**: definição das entidades da aplicação.
* **Middlewares**: tratamento centralizado de erros e processamento das requisições.
* **Testes**: testes unitários e de integração.


# Vehicle Management API - Technical Challenge

REST API developed with Node.js, TypeScript and Express for managing vehicles, drivers and vehicle usage records.

## Features

### Vehicles

* Create a vehicle
* Update a vehicle
* Delete a vehicle
* Get vehicle by ID
* List vehicles
* Filter vehicles by color
* Filter vehicles by brand

### Drivers

* Create a driver
* Update a driver
* Delete a driver
* Get driver by ID
* List drivers
* Filter drivers by name

### Vehicle Usage

* Start vehicle usage
* Finish vehicle usage
* List all vehicle usage records
* Show driver and vehicle information in usage records

## Business Rules

* A vehicle can only be used by one driver at a time.
* A driver already using a vehicle cannot use another vehicle simultaneously.

## Technologies

* Node.js
* TypeScript
* Express
* Jest
* Supertest
* UUID

## Live Demo

Base URL:

https://vehicle-management-api-seidor.onrender.com

The API is deployed and can be tested using Postman or any HTTP client.

Note: This project uses in-memory persistence, so all data will be reset when the server restarts (e.g., Render redeploys or idle restart).

### Example Endpoints

#### Cars
- GET /cars
- POST /cars
- GET /cars?color=Black&brand=Toyota

#### Drivers
- GET /drivers
- POST /drivers
- GET /drivers?name=Bryan

#### Vehicle Usage
- GET /usages
- POST /usages
- PATCH /usages/:id/finish

## Installation

Clone the repository:

```bash
git clone <repository-url>
```

Install dependencies:

```bash
npm install
```

## Running the Application

Development mode:

```bash
npm run dev
```

The API will be available at:

```text
http://localhost:3000
```

## Running Tests

```bash
npm test
```

## API Endpoints

### Vehicles

| Method | Endpoint  |
| ------ | --------- |
| POST   | /cars     |
| GET    | /cars     |
| GET    | /cars/:id |
| PUT    | /cars/:id |
| DELETE | /cars/:id |

### Drivers

| Method | Endpoint     |
| ------ | ------------ |
| POST   | /drivers     |
| GET    | /drivers     |
| GET    | /drivers/:id |
| PUT    | /drivers/:id |
| DELETE | /drivers/:id |

### Vehicle Usage

| Method | Endpoint           |
| ------ | ------------------ |
| POST   | /usages            |
| PATCH  | /usages/:id/finish |
| GET    | /usages            |

## Tests

The project includes:

* Unit tests for services
* Integration tests for API endpoints
* Business rule validation tests

## Project Structure

```text
src
├── controllers
├── services
├── repositories
├── routes
├── models
├── middlewares
├── tests
├── container.ts
├── app.ts
└── server.ts
```

### Architecture

The application follows a layered architecture:

```text
Request
   ↓
Routes
   ↓
Controllers
   ↓
Services
   ↓
Repositories
   ↓
In-Memory Storage
```

#### Responsibilities

* **Routes**: endpoint definitions.
* **Controllers**: handle HTTP requests and responses.
* **Services**: implement business rules and application logic.
* **Repositories**: manage in-memory data persistence.
* **Models**: define application entities.
* **Middlewares**: centralized error handling and request processing.
* **Tests**: unit and integration tests.
