# Plano Backend 30 Dias (Nivel Mercado)

## Objetivo
Evoluir de backend funcional para backend pronto para ambiente de producao.

## Carga sugerida
- 1h a 2h por dia
- Formato diario: 20% teoria + 80% pratica

## Ordem de prioridade
1. Banco de dados e performance SQL
2. Testes (unitario, integracao, API)
3. Seguranca aplicada
4. Observabilidade e operacao
5. Consolidacao com projeto final

## Semana 1 - Banco e Performance SQL (Dias 1 a 7)
### Meta
Sair do SQL que funciona para SQL que escala.

### Foco
- Modelagem relacional
- Indices simples e compostos
- EXPLAIN e plano de execucao
- Transacoes e isolamento
- Locks (otimista e pessimista)
- Paginacao eficiente

### Entregavel da semana
- 3 queries reais otimizadas
- comparativo antes/depois
- documento de trade-offs

## Semana 2 - Testes de Verdade (Dias 8 a 14)
### Meta
Refatorar com seguranca sem quebrar fluxo critico.

### Foco
- Piramide de testes
- Testes unitarios para regra de negocio
- Testes de integracao com banco
- Testes de API (contrato e comportamento)
- Mocks e stubs com criterio

### Entregavel da semana
- Suite completa de 1 fluxo critico
- cenarios de sucesso e erro
- relatorio de qualidade dos testes

## Semana 3 - Seguranca Aplicada (Dias 15 a 21)
### Meta
Reduzir risco real em producao.

### Foco
- JWT bem implementado (expiracao, refresh, revogacao)
- Autorizacao por escopo/permissao
- Validacao de entrada
- OWASP Top 10 aplicado
- Rate limiting e anti abuso

### Entregavel da semana
- hardening de 2 a 3 endpoints
- checklist de seguranca por endpoint
- evidencias de testes de ataque basico

## Semana 4 - Observabilidade e Operacao (Dias 22 a 28)
### Meta
Diagnosticar problemas em producao com rapidez.

### Foco
- Logs estruturados
- Correlacao de requisicoes
- Metricas de latencia, erro e throughput
- Alertas basicos
- Tracing distribuido (fundamentos)
- Fluxo de rollback seguro

### Entregavel da semana
- painel simples de metricas
- guia de incidente (passo a passo)
- instrumentacao de 1 fluxo ponta a ponta

## Dias 29 e 30 - Projeto Final
### Meta
Consolidar tudo em uma entrega pronta para producao.

### Escopo minimo
- 1 modulo real com melhorias de SQL
- testes unitarios + integracao + API
- reforco de seguranca
- logs e metricas
- documento de decisoes tecnicas

## Criterios de evolucao
- Explica o por que tecnico de cada decisao
- Mede melhoria (tempo, erro, cobertura, latencia)
- Registra trade-offs de forma clara
- Consegue reproduzir e corrigir falhas sem adivinhacao

## Regra pratica
Nao tentar estudar tudo de uma vez.
Avanco consistente > estudo volumoso e desconectado da pratica.
