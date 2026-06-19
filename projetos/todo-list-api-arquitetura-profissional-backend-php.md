
## 📌 Descrição

API de gerenciamento de tarefas desenvolvida com foco em boas práticas de engenharia de software, incluindo:

- Arquitetura em camadas
    
- Princípios SOLID
    
- Padrões de projeto
    
- Preparação para evolução em microserviços
    

O projeto simula um cenário real de mercado, indo além de um simples CRUD.

---

# 🎯 Objetivo

Criar uma API robusta e escalável que permita:

- Gerenciamento de usuários
    
- Autenticação segura
    
- Criação e controle de tarefas
    
- Estrutura preparada para crescimento e distribuição
    

---

# 🧱 Arquitetura

## 🔹 Padrão adotado

Arquitetura em camadas com inspiração em Clean Architecture + DDD leve.

---

## 📂 Estrutura de pastas

```
app/
 ├── Http/
 │    ├── Controllers/
 │    ├── Requests/
 │
 ├── Domain/
 │    ├── Entities/
 │    ├── Enums/
 │
 ├── Services/
 ├── Repositories/
 ├── DTOs/
 ├── Exceptions/
```

---

## 🔄 Fluxo da aplicação

```
Request → Controller → Service → Repository → Banco
                         ↓
                      Domain
```

---

## 🧩 Responsabilidades

### Controller

- Recebe requisições HTTP
    
- Valida entrada
    
- Retorna resposta
    

### Service

- Contém regras de negócio
    
- Orquestra o fluxo da aplicação
    

### Repository

- Abstrai acesso ao banco
    
- Centraliza queries
    

### Domain

- Representa o núcleo do sistema
    
- Contém entidades e regras
    

### DTO

- Padroniza entrada e saída de dados
    

---

# 🧠 Modelagem de Domínio

## 👤 User

- id
    
- name
    
- email
    
- password
    

## ✅ Task

- id
    
- user_id
    
- title
    
- description
    
- status
    
- priority
    
- due_date
    

---

## 📌 Regras de negócio

- Task deve ter título obrigatório
    
- Task pertence a um usuário
    
- Status pode ser alterado
    
- Prioridade influencia ordenação
    

---

# ⚙️ Tecnologias

- PHP
    
- Laravel
    
- MySQL
    
- JWT (autenticação)
    

---

# 🔐 Autenticação

- Login com JWT
    
- Rotas protegidas
    
- Middleware de autenticação
    

---

# 📡 Endpoints

## 🔑 Auth

### POST /register

Cria um usuário

### POST /login

Retorna token JWT

---

## 👤 User

### GET /me

Retorna dados do usuário autenticado

---

## ✅ Tasks

### POST /tasks

Cria tarefa

### GET /tasks

Lista tarefas

### PUT /tasks/{id}

Atualiza tarefa

### DELETE /tasks/{id}

Remove tarefa

---

# 🧪 Testes

- Testes unitários (Services)
    
- Testes de integração (Endpoints)
    

---

# ⚡ Performance

- Paginação de resultados
    
- Possível uso futuro de cache
    

---

# 🔐 Segurança

- Hash de senha
    
- Proteção de rotas
    
- Validação de entrada
    

---

# 🚀 Evolução do Projeto

## 🥇 Fase 1 — Monolito

- API completa
    
- Arquitetura limpa
    

## 🥈 Fase 2 — Modularização

- Separação por domínio
    

## 🥉 Fase 3 — Microserviços

- User Service
    
- Task Service
    

## 🏁 Fase 4 — Event-driven

- Mensageria (RabbitMQ/Kafka)
    
- Processamento assíncrono
    

---

# 💡 Decisões Técnicas

- Uso de arquitetura em camadas para organização
    
- Aplicação de SOLID para código sustentável
    
- Repository Pattern para desacoplamento do banco
    
- Preparação para microserviços desde o início
    
- Separação clara de domínios (User / Task)
    

---

# 📊 Diagrama simples

```
Controller → Service → Repository → Database
```

---

# 🧠 Conceitos aplicados

- SOLID
    
- Design Patterns (Strategy, Repository)
    
- DDD (básico)
    
- Clean Architecture (inspirado)
    
- REST API
    

---

# ⚠️ Considerações

- Projeto iniciado como monolito por simplicidade
    
- Estrutura preparada para escalar
    
- Foco em clareza e manutenção
    

---

# 🚀 Como rodar o projeto

```bash
git clone <repo>
cd projeto

composer install
cp .env.example .env

php artisan key:generate
php artisan migrate

php artisan serve
```

---

# 📌 Próximos passos

- Implementar cache
    
- Adicionar mensageria
    
- Criar testes mais robustos
    
- Adicionar front-end (React ou Vue)
    

---

# 🏁 Conclusão

Este projeto foi desenvolvido com foco em simular um ambiente real de desenvolvimento backend, priorizando:

- Boas práticas
    
- Escalabilidade
    
- Organização de código
    
- Preparação para sistemas distribuídos