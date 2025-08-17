# Arquitetura — Visão Geral

```mermaid
flowchart LR
  User[User/Client] --> API[API Gateway/Ingress]
  API --> APP[InnerAI Backend (Spring Boot)]
  APP -->|Cache| Redis[(Redis)]
  APP -->|Metadados| Postgres[(Postgres)]
  APP -->|Objetos| MinIO[(S3/MinIO)]
  APP -->|Métricas/Logs| OTel[OpenTelemetry]
  APP -->|Providers| Ext[OpenAI/Anthropic/Gemini/...]
```

- **Backend**: Spring Boot 3, WebFlux (para IO-bound), Resilience4j (circuit breaker, retry, rate limit).
- **Banco**: Postgres para entidades de projeto, chaves, logs de alto nível.
- **Cache**: Redis para throttling, locks, counters.
- **Storage**: MinIO (S3 compatível) para exportações/artefatos.
- **Observabilidade**: OpenTelemetry + Prometheus + Loki (dev).

## Componentes (MVP)
- **Identity & Projects**: projetos, tokens, RBAC simples.
- **Provider Manager**: credenciais, modelos permitidos, teste de saúde.
- **Router**: seleção explícita e fallback.
- **Prompt Templates**: CRUD + render.
- **Usage & Logs**: agregações e export.
