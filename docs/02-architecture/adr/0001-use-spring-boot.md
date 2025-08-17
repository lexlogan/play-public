# ADR-0001 — Spring Boot e WebFlux
- **Decisão**: Usar Spring Boot 3 + WebFlux para IO-bound.
- **Motivação**: Latência e escala para chamadas externas.
- **Consequências**: Programação reativa; atenção a backpressure.
