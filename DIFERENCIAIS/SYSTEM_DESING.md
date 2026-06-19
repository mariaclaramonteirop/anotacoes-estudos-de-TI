# Roadmap Completo — System Design + DevOps

---

# Visão Geral

Este roadmap une:
- Back-end
- System Design
- DevOps
- Cloud
- Arquitetura Distribuída

Objetivo:
Construir conhecimento do básico ao avançado para atuar como:
- Backend Engineer
- Software Engineer
- DevOps Engineer
- Platform Engineer
- SRE

---

# ROADMAP SYSTEM DESIGN

# FASE 1 — FUNDAMENTOS

## Redes e HTTP
- [ ] Como funciona uma requisição HTTP
- [ ] HTTP Methods
- [ ] Headers
- [ ] Cookies vs Sessions
- [ ] JWT
- [ ] HTTPS/SSL
- [ ] DNS
- [ ] TCP/IP
- [ ] Latência
- [ ] WebSockets
- [ ] HTTP/1 vs HTTP/2

---

## APIs
- [ ] REST
- [ ] RESTful conventions
- [ ] Versionamento
- [ ] Idempotência
- [ ] Rate limit
- [ ] Paginação
- [ ] Upload de arquivos
- [ ] OpenAPI/Swagger

---

## Banco de Dados
- [ ] Modelagem relacional
- [ ] Índices
- [ ] JOINs
- [ ] Transactions
- [ ] ACID
- [ ] Locks
- [ ] Isolation Levels
- [ ] Query optimization
- [ ] EXPLAIN ANALYZE

---

## NoSQL
- [ ] Documento
- [ ] Chave-valor
- [ ] Wide-column
- [ ] Graph databases
- [ ] Quando usar NoSQL

---

## Docker
- [ ] Containers
- [ ] Dockerfile
- [ ] Docker Compose
- [ ] Volumes
- [ ] Networks
- [ ] Multi-stage build

---

# FASE 2 — ESCALABILIDADE

## Cache
- [ ] O que é cache
- [ ] Redis
- [ ] Cache Aside
- [ ] Write Through
- [ ] TTL
- [ ] Cache invalidation
- [ ] Distributed cache

---

## Load Balancer
- [ ] Round Robin
- [ ] Least Connections
- [ ] Sticky Sessions
- [ ] Reverse Proxy
- [ ] Nginx

---

## CDN
- [ ] Conceito
- [ ] Edge servers
- [ ] Cache global
- [ ] Assets estáticos

---

## Escalabilidade
- [ ] Vertical Scaling
- [ ] Horizontal Scaling
- [ ] Stateless applications
- [ ] Session sharing

---

## Replicação e Sharding
- [ ] Read replicas
- [ ] Primary/Replica
- [ ] Database sharding
- [ ] Consistent hashing

---

# FASE 3 — SISTEMAS DISTRIBUÍDOS

## Message Brokers
- [ ] RabbitMQ
- [ ] Kafka
- [ ] Queue
- [ ] Topic
- [ ] Producer/Consumer
- [ ] Retry
- [ ] DLQ
- [ ] Event-driven architecture

---

## Microsserviços
- [ ] Service decomposition
- [ ] API Gateway
- [ ] Service Discovery
- [ ] Comunicação síncrona
- [ ] Comunicação assíncrona

---

## Consistência
- [ ] CAP Theorem
- [ ] Strong consistency
- [ ] Eventual consistency
- [ ] Distributed transactions

---

## Resiliência
- [ ] Retry
- [ ] Timeout
- [ ] Circuit Breaker
- [ ] Bulkhead
- [ ] Idempotência

---

## Observabilidade
- [ ] Logs centralizados
- [ ] Metrics
- [ ] Tracing
- [ ] OpenTelemetry
- [ ] Prometheus
- [ ] Grafana

---

# FASE 4 — AVANÇADO

## Kubernetes
- [ ] Pods
- [ ] Deployments
- [ ] Services
- [ ] Ingress
- [ ] ConfigMaps
- [ ] Secrets
- [ ] Autoscaling

---

## Arquitetura Avançada
- [ ] CQRS
- [ ] Event Sourcing
- [ ] Saga Pattern
- [ ] Outbox Pattern
- [ ] Service Mesh
- [ ] Distributed locks

---

## Cloud
- [ ] AWS básico
- [ ] EC2
- [ ] S3
- [ ] RDS
- [ ] Load Balancer
- [ ] ECS/EKS
- [ ] IAM

---

# ROADMAP DEVOPS

# FASE 1 — FUNDAMENTOS

## Linux
- [ ] Navegação terminal
- [ ] Permissões
- [ ] Usuários e grupos
- [ ] SSH
- [ ] Variáveis de ambiente
- [ ] Processos
- [ ] systemctl
- [ ] logs
- [ ] grep/sed/awk
- [ ] pipes
- [ ] bash scripting

---

## Redes
- [ ] DNS
- [ ] HTTP/HTTPS
- [ ] TCP/IP
- [ ] Portas
- [ ] Proxy
- [ ] Reverse proxy
- [ ] SSL/TLS
- [ ] Firewall

---

## Git Avançado
- [ ] Rebase
- [ ] Cherry-pick
- [ ] Gitflow
- [ ] Hooks
- [ ] Tags
- [ ] Versionamento semântico

---

# FASE 2 — CONTAINERS

## Docker
- [ ] Containers
- [ ] Images
- [ ] Dockerfile
- [ ] Volumes
- [ ] Networks
- [ ] Multi-stage builds
- [ ] Docker Compose
- [ ] Otimização de imagem
- [ ] Healthcheck

---

## Projeto prático
- [ ] Containerizar API PHP
- [ ] Banco PostgreSQL
- [ ] Redis
- [ ] RabbitMQ
- [ ] Nginx

---

# FASE 3 — CI/CD

## CI (Continuous Integration)
- [ ] Build automático
- [ ] Testes automatizados
- [ ] Lint
- [ ] Quality Gate

---

## CD (Continuous Delivery/Deployment)
- [ ] Deploy automatizado
- [ ] Rollback
- [ ] Blue-Green deploy
- [ ] Canary deploy

---

## Ferramentas
- [ ] GitHub Actions
- [ ] GitLab CI
- [ ] Jenkins

---

# FASE 4 — CLOUD

## Conceitos Cloud
- [ ] IaaS
- [ ] PaaS
- [ ] SaaS

---

## AWS Core
- [ ] EC2
- [ ] S3
- [ ] IAM
- [ ] RDS
- [ ] VPC
- [ ] Route53
- [ ] Load Balancer
- [ ] Auto Scaling

---

## Deploy real
- [ ] Deploy API
- [ ] Configurar domínio
- [ ] HTTPS
- [ ] Backup
- [ ] Monitoramento

---

# FASE 5 — INFRAESTRUTURA COMO CÓDIGO

## Terraform
- [ ] Providers
- [ ] Resources
- [ ] Variables
- [ ] Outputs
- [ ] State
- [ ] Modules

---

# FASE 6 — KUBERNETES

## Kubernetes
- [ ] Pod
- [ ] Deployment
- [ ] ReplicaSet
- [ ] Service
- [ ] Ingress
- [ ] ConfigMap
- [ ] Secret
- [ ] Namespace
- [ ] Autoscaling

---

## Kubernetes Avançado
- [ ] Helm
- [ ] StatefulSets
- [ ] DaemonSets
- [ ] Persistent Volumes
- [ ] Operators

---

# FASE 7 — OBSERVABILIDADE

## Logs
- [ ] ELK Stack
- [ ] Loki

---

## Metrics
- [ ] Prometheus
- [ ] Grafana

---

## Tracing
- [ ] OpenTelemetry
- [ ] Jaeger

---

# FASE 8 — SEGURANÇA

## DevSecOps
- [ ] Secrets management
- [ ] Vault
- [ ] IAM
- [ ] Least privilege
- [ ] Vulnerability scanning
- [ ] Container scanning
- [ ] SSL/TLS
- [ ] WAF

---

# FASE 9 — AVANÇADO

## Service Mesh
- [ ] Istio
- [ ] Linkerd

---

## GitOps
- [ ] ArgoCD
- [ ] FluxCD

---

## Platform Engineering
- [ ] Internal Developer Platform
- [ ] Self-service infrastructure

---

# ROTINA DE ESTUDOS

# Segunda — Linux + Redes
## Objetivo
Infraestrutura e fundamentos

## Estudar
- SSH
- systemctl
- nginx
- DNS
- HTTP
- TCP/IP

## Prática
- Configurar servidor Linux
- Criar reverse proxy

---

# Terça — Docker + Containers
## Objetivo
Containerização

## Estudar
- Docker
- Docker Compose
- Networks
- Volumes

## Prática
- Containerizar API
- Subir PostgreSQL
- Integrar Redis

---

# Quarta — Banco + Escalabilidade
## Objetivo
Performance

## Estudar
- Índices
- Replicação
- Cache
- Sharding

## Prática
- Redis cache
- Query optimization

---

# Quinta — CI/CD + Cloud
## Objetivo
Deploy automatizado

## Estudar
- GitHub Actions
- AWS
- Deploy pipelines

## Prática
- Pipeline automática
- Deploy EC2

---

# Sexta — Microsserviços + Mensageria
## Objetivo
Arquitetura distribuída

## Estudar
- RabbitMQ
- Kafka
- Event-driven

## Prática
- Producer/Consumer
- Retry
- DLQ

---

# Sábado — Kubernetes + Observabilidade
## Objetivo
Orquestração e monitoramento

## Estudar
- Kubernetes
- Prometheus
- Grafana

## Prática
- Deploy Kubernetes
- Configurar métricas

---

# Domingo — Projeto Real
## Objetivo
Consolidar conhecimento

## Projeto recomendado
Plataforma financeira/event-driven

### Serviços
- Auth Service
- User Service
- Wallet Service
- Transaction Service
- Notification Service

### Infraestrutura
- API Gateway
- RabbitMQ/Kafka
- Redis
- PostgreSQL
- Docker
- Kubernetes

### Observabilidade
- Prometheus
- Grafana
- Loki

---

# ARQUITETURA SUGERIDA

```txt
Internet
   │
Cloudflare
   │
Load Balancer
   │
Kubernetes
   │
├── API Gateway
├── Auth Service
├── Wallet Service
├── Notification Service
│
├── RabbitMQ/Kafka
├── Redis
├── PostgreSQL
│
├── Prometheus
├── Grafana
└── Loki