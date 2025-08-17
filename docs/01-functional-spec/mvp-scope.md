# MVP — Ordem de Implementação

1) **Fundação**
   - Projeto Spring Boot base, autenticação por token de projeto.
   - Postgres + Redis no Docker Compose.
   - Estrutura de domínios: Projects, ApiTokens, Providers, Models.

2) **Gestão de Provedores**
   - Endpoints CRUD de credenciais.
   - Teste de conectividade (health-check por provedor).

3) **Completions v1**
   - Endpoint unificado `/v1/completions` (text-only) com `provider+model` explícitos.
   - Fallback simples (ordem estática por projeto).
   - Logging/metrics.

4) **Playground Web (básico)**
   - Tela única com prompt, seleção de provedores e comparação.
   - Histórico recente por projeto.

5) **Templates de Prompt**
   - CRUD + renderização com variáveis.

6) **Observabilidade/Export**
   - Endpoint `/v1/usage/metrics` e `/v1/logs/export` (CSV).

7) **Políticas simples**
   - Limites RPM/TPM e `circuit breaker` por provedor/projeto.

> Cada etapa deve finalizar com testes de contrato e smoke tests via CI.
