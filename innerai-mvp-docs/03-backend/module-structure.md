# Estrutura sugerida (Mono-repo, módulo único no MVP)

```
backend/
  src/main/java/com/innerai/
    api/        # controllers (webflux)
    app/        # casos de uso, services
    domain/     # entidades e portas
    infra/      # adapters: db, redis, http clients, security
  src/main/resources/
    application.yaml
```

- **WebFlux** para IO-bound (chamadas externas).
- **Resilience4j** para retry/circuit breaker/ratelimit.
- **MapStruct** para mapeamentos.
- **Spring Security** para bearer tokens.
