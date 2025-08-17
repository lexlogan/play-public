# Estratégia de Testes

- **Unitários**: serviços, templates, roteamento.
- **Contratos**: WireMock para provedores.
- **Integração**: Testcontainers (Postgres/Redis).
- **E2E**: smoke tests do `/v1/completions` com provedores mock.
- **Performance**: Gatling/k6 para p95 e throughput.
