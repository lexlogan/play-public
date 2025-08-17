# cURL — Exemplos

```bash
# Listar projetos
curl -H "Authorization: Bearer <ADMIN_JWT>" http://localhost:8080/v1/projects

# Completion explícito
curl -X POST http://localhost:8080/v1/completions   -H "Authorization: Bearer <PROJECT_TOKEN>"   -H "Content-Type: application/json"   -d '{
    "projectId": "00000000-0000-0000-0000-000000000000",
    "provider": "openai",
    "model": "gpt-4o-mini",
    "prompt": "Escreva um haicai sobre servidores Kubernetes."
  }'
```
