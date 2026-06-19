# Checklist Backend (Nível Mercado)

## 1. Fundamentos de Programação
- [ ] Estruturas de dados (listas, filas, pilhas, arvores, grafos)
- [ ] Complexidade de algoritmos (Big O)
- [ ] Programacao orientada a objetos (POO)
- [ ] Baixo acoplamento e alta coesao

## 2. Backend Essencial
- [ ] APIs REST (boas praticas)
- [ ] Metodos HTTP (GET, POST, PUT, PATCH, DELETE)
- [ ] Status codes
- [ ] Validacao de dados
- [ ] Serializacao (JSON)
- [ ] Contrato de API (request/response consistente)
- [ ] Paginacao, filtro e ordenacao em listagens
- [ ] Documentacao de API (OpenAPI/Swagger)

## 3. Arquitetura Basica
- [ ] Arquitetura em camadas (Controller, Service, Repository)
- [ ] Separacao de responsabilidades
- [ ] Organizacao de pastas e modulos
- [ ] DTOs e mapeamento entre camadas
- [ ] Configuracao por ambiente (12-factor app)

## 4. Design Patterns
### Criacionais
- [ ] Factory
- [ ] Singleton

### Estruturais
- [ ] Adapter
- [ ] Decorator

### Comportamentais
- [ ] Strategy
- [ ] Observer

### Aplicacao em backend
- [ ] Repository Pattern

## 5. SOLID
- [ ] Single Responsibility Principle
- [ ] Open/Closed Principle
- [ ] Liskov Substitution Principle
- [ ] Interface Segregation Principle
- [ ] Dependency Inversion Principle

## 6. DDD (Domain-Driven Design)
- [ ] Entidades
- [ ] Value Objects
- [ ] Aggregates
- [ ] Repositories
- [ ] Domain Services
- [ ] Bounded Context
- [ ] Linguagem ubiqua

## 7. Arquiteturas de Software
- [ ] MVC (Model-View-Controller)
- [ ] MVVM (Model-View-ViewModel)
- [ ] Clean Architecture
- [ ] Arquitetura Hexagonal (Ports and Adapters)
- [ ] Monolito vs Microservicos

## 8. System Design
- [ ] Escalabilidade (vertical vs horizontal)
- [ ] Load balancing
- [ ] Cache (ex: Redis)
- [ ] Mensageria (ex: RabbitMQ, Apache Kafka)
- [ ] Consistencia de dados
- [ ] Idempotencia
- [ ] Rate limiting

## 9. Banco de Dados
- [ ] Modelagem relacional
- [ ] SQL avancado
- [ ] Indices
- [ ] Transacoes
- [ ] Lock otimista vs pessimista
- [ ] NoSQL (quando usar)
- [ ] Migrations e rollback seguro
- [ ] Integridade referencial e constraints

## 10. Concorrencia e Assincronismo
- [ ] Threads / async
- [ ] Race conditions
- [ ] Deadlocks
- [ ] Processamento assincrono
- [ ] Filas

## 11. Testes
- [ ] Testes unitarios
- [ ] Testes de integracao
- [ ] Testes de API
- [ ] Mocks e stubs
- [ ] Cobertura de testes
- [ ] Testes de contrato
- [ ] Testes de regressao

## 12. Seguranca
- [ ] Autenticacao (JWT, OAuth)
- [ ] Autorizacao
- [ ] Hash de senha (bcrypt)
- [ ] OWASP Top 10
- [ ] SQL Injection
- [ ] XSS / CSRF
- [ ] Gestao de secrets (nao hardcode)
- [ ] CORS e headers de seguranca

## 13. Comunicacao entre Sistemas
- [ ] HTTP (headers, caching)
- [ ] WebSockets
- [ ] gRPC
- [ ] GraphQL

## 14. Performance
- [ ] Cache (ex: Redis)
- [ ] Paginacao
- [ ] Lazy loading
- [ ] Compressao
- [ ] Otimizacao de queries
- [ ] Benchmark e profiling
- [ ] Connection pooling

## 15. Observabilidade
- [ ] Logs estruturados
- [ ] Metricas
- [ ] Tracing distribuido
- [ ] Prometheus
- [ ] Grafana
- [ ] ELK Stack
- [ ] Correlation ID por requisicao
- [ ] Alertas e SLO/SLA

## 16. Arquiteturas Avancadas
- [ ] Event-driven architecture
- [ ] CQRS
- [ ] Event sourcing

## 17. DevOps Basico
- [ ] Containers (Docker)
- [ ] CI/CD
- [ ] Ambientes (dev, staging, prod)
- [ ] IaC (Infra as Code) - fundamentos
- [ ] Estrategia de deploy e rollback

## 18. Produto e Engenharia
- [ ] Trade-offs tecnicos
- [ ] Pensamento orientado a negocio
- [ ] Evolucao de sistema
- [ ] Versionamento de API

## 19. Resiliencia e Operacao
- [ ] Timeouts e retries com backoff
- [ ] Circuit breaker e bulkhead (conceitos)
- [ ] Health checks (liveness/readiness)
- [ ] Graceful shutdown
- [ ] Idempotencia em operacoes criticas

---

## Como usar este checklist
Nao tente fazer tudo de uma vez.

### Ordem recomendada
1. Fundamentos + backend essencial
2. Arquitetura + SOLID + patterns
3. Banco + testes
4. System design + concorrencia
5. Avancado (DDD + mensageria + observabilidade)
