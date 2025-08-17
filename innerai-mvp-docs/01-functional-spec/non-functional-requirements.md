# Requisitos Não Funcionais

- **Disponibilidade** (MVP): 99,5% alvo.
- **Latência**: p95 < 1.5s para completions simples (rede variável).
- **Segurança**: segredos criptografados em repouso; TLS em trânsito.
- **Observabilidade**: logs estruturados, métricas (latência, erros, tokens).
- **Escalabilidade**: stateless app, horizontal scaling.
- **Portabilidade**: dev local via Docker Compose; prod em EKS.
