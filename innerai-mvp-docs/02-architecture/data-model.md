# Modelo de Dados (ERD simplificado, Mermaid)

```mermaid
erDiagram
  PROJECT ||--o{ API_TOKEN : has
  PROJECT ||--o{ PROVIDER_CREDENTIAL : manages
  PROJECT ||--o{ PROMPT_TEMPLATE : owns
  PROJECT ||--o{ USAGE_LOG : tracks

  PROJECT {
    uuid id PK
    text name
    text slug
    timestamptz created_at
  }

  API_TOKEN {
    uuid id PK
    uuid project_id FK
    text name
    text hashed_token
    text scopes
    bool active
    timestamptz created_at
    timestamptz revoked_at
  }

  PROVIDER_CREDENTIAL {
    uuid id PK
    uuid project_id FK
    text provider  // openai, anthropic, google, azure
    text environment // dev, stage, prod
    text key_ref // referencia segura
    jsonb config // models permitidos, fallback order
    bool active
    timestamptz created_at
  }

  PROMPT_TEMPLATE {
    uuid id PK
    uuid project_id FK
    text name
    text version
    text content
    jsonb metadata
    timestamptz created_at
  }

  USAGE_LOG {
    uuid id PK
    uuid project_id FK
    text request_id
    text provider
    text model
    int input_tokens
    int output_tokens
    int http_status
    numeric latency_ms
    jsonb error
    timestamptz created_at
  }
```
