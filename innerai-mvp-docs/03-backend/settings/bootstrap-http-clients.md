# HTTP Clients (WebClient)

- Configure `WebClient` por provedor com `baseUrl`, `defaultHeaders` dinâmicos (por projeto).
- `ExchangeFilterFunction` para `requestId`, `timing` e logs estruturados.
- Use `Resilience4j` decorators: `Retry`, `CircuitBreaker`, `RateLimiter` por provedor/projeto.
