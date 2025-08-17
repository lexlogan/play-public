# Observabilidade (MVP)

- **Tracing**: OpenTelemetry SDK no Spring Boot → OTLP (Collector). 
- **Métricas**: Micrometer → Prometheus (ou Collector → logging no dev).
- **Logs**: JSON estruturado; correlação por `requestId`.

KPIs básicos:
- Latência p50/p95 por provedor e por rota.
- Taxa de erro (HTTP 5xx/4xx).
- Tokens in/out por projeto.
