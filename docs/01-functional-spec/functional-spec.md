# Especificação Funcional

## Escopo do MVP

1. **Autenticação & Autorização**
   - Cadastro de organização (tenant) e projetos.
   - RBAC simples: `ADMIN`, `USER` no escopo do projeto.
   - Tokens de API por projeto (escopo: read/write/usage).

2. **Gestão de Provedores**
   - Registrar credenciais por provedor (OpenAI, Anthropic, Google/Vertex ou Gemini, Azure OpenAI).
   - Marcar credenciais por ambiente (dev/stage/prod).
   - Teste de conectividade e quota básica.

3. **Roteamento de Requisições**
   - Modo explícito: usuário escolhe `provider+model`.
   - Fallback simples: ordem de preferência predefinida no projeto.
   - Limites por projeto (RPM/TPM) e circuit breaker básico por provedor.

4. **Playground**
   - UI para criar prompts, escolher provedores e comparar respostas lado a lado.
   - Histórico local do projeto (últimos N prompts).

5. **Templates de Prompt**
   - CRUD de prompts parametrizáveis (nome, tags, versão).
   - Renderização com variáveis e pré-visualização.

6. **Observabilidade & Uso**
   - Log de chamadas (projectId, provider, model, tokens in/out, status, latência).
   - Métricas agregadas por período.
   - Export CSV/NDJSON.

7. **Segurança**
   - Storage de segredos seguro (MVP: KMS local + env/file; produção: AWS KMS/Secrets Manager).
   - Auditoria básica de operações sensíveis.

## Fora do MVP (Roadmap)
- A/B routing, ranking automático por qualidade/latência.
- Cache semântico, embeddings e RAG nativo.
- Fine-tuning management.
- Multi-tenant SSO (SAML/OIDC), SCIM.
- Cotas e billing interno.
