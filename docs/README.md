# InnerAI-like Platform — MVP Documentation Pack

**Data do pacote:** 2025-08-13

Este pacote contém documentação funcional e técnica, especificações de API, modelos de dados,
diagramação em Mermaid, exemplos de automação e arquivos de suporte (Docker Compose, CI)
para construir um MVP de uma plataforma agregadora de LLMs (semelhante ao InnerAI).

## Estrutura

```
innerai-mvp-docs/
├─ 00-product-vision/
├─ 01-functional-spec/
├─ 02-architecture/
├─ 03-backend/
├─ 04-ops/
├─ 05-ux/
├─ 06-samples/
└─ LICENSE
```

## Como usar rapidamente

1. Leia `00-product-vision/vision.md` para alinhar objetivos de produto.
2. Revise o **MVP** em `01-functional-spec/mvp-scope.md` e o **backlog** em `user-stories.md`.
3. Confira `02-architecture/architecture-overview.md` e `openapi.yaml`.
4. Rode o ambiente local com Docker:
   ```bash
   cd 02-architecture
   cp .env.example .env
   docker compose up -d
   ```
5. Use `06-samples/postman_collection.json` ou `06-samples/curl-examples.md` para testar endpoints stubados.
6. Acompanhe `04-ops/ci-cd.md` e `observability.md` para práticas de entrega e visibilidade.
