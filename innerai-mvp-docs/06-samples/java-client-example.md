# Exemplo Java (WebClient)

```java
WebClient client = WebClient.builder()
    .baseUrl("http://localhost:8080")
    .defaultHeader(HttpHeaders.AUTHORIZATION, "Bearer " + projectToken)
    .build();

Mono<String> res = client.post()
    .uri("/v1/completions")
    .contentType(MediaType.APPLICATION_JSON)
    .bodyValue(Map.of(
        "projectId", projectId.toString(),
        "provider", "openai",
        "model", "gpt-4o-mini",
        "prompt", "Hello from Java"
    ))
    .retrieve()
    .bodyToMono(String.class);
```
